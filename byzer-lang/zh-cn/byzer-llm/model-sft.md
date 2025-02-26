## Byzer-LLM 模型微调

> 2023-06-25

截止到本文撰写为止，Byzer-LLM 默认使用 QLora 进行单机多卡微调，多机多卡全参数预训练的支持工作正在进行中。

## 已经测试过支持微调的模型(截止至2023-06-26)

1. custom/chatglm2
2. custom/baichuan
3. custom/falcon

其中 

1. chatglm2 需要 pytorch 2.0.1 才能在消费级显卡上微调 （flash attension的限制）
2. chatglm2 需要修改模型权重文件目录里的 tokenization_chatglm.py 第 72 行代码。在其后添加一条新语句（bug，等待官方修复）：

```python
self.vocab_file = vocab_file
```


## 数据格式

Byzer-LLM 微调支持两种QA格式的数据。

第一种是 Alpaca 格式

```
instruction string
input string
output string
history array<array<string>>
```

第二种是 Moss 格式：

```
category  string
conversation array<struct<assistant:string,human:string>>
conversation_id bigint
dataset string
```

## 微调步骤

加载数据和模型：

```sql
load json.`file:///home/winubuntu/projects/Firefly/data/dummy_data.jsonl` where
inferSchema="true"
as sft_data;

load delta.`ai_model.baichuan_7B_model` as baichuan_7B_model;
```


```sql

-- 模型微调
!byzerllm setup sft;

run command as LLM.`` where 
and localPathPrefix="/my8t/byzerllm/jobs"
and pretrainedModelType="custom/baichuan"
and model="baichuan_7B_model"
and inputTable="sft_data"
and outputTable="baichuan300"
and `sft.int.max_seq_length`="512";

-- 保存模型
save overwrite baichuan300 as delta.`ai_model.baichuan300`;
```

如果使用数据湖拉取模型并保存，需要额外消耗18-30分钟（26g左右大小的模型文件夹）。正常情况考虑到微调的较长的实际运行时间，这点额外开销微不足道。
不过很多时候我们需要快速进行测试，并且减少资源消耗，这个时候可以使用提前放在训练机器上的本地模型，代码如下：


```sql
!byzerllm setup sft;

run command as LLM.`` where 
and localPathPrefix="/my8t/byzerllm/jobs"
and pretrainedModelType="custom/baichuan"
and model="command"
and localModelDir="/home/winubuntu/projects/baichuan-7B-model"
and inputTable="sft_data"
and outputTable="baichuan300"
and `sft.int.max_seq_length`="512";

-- 保存模型
save overwrite baichuan300 as delta.`ai_model.baichuan300`;
```

相比之前的代码，我们把 model 修改为 command, 同时添加 localModelDir 显式指定原始模型路径。

其中 `sft.int.max_seq_length` 用来指定微调参数。该参数由三部分构成：

1. sft 参数前缀
2. int  参数类型
3. max_seq_length 参数名称

下面是是一些默认参数列表，同时为您提供了可配置的参数列表：

```json
DEFAULT_QLORA_CONFIG = {    
    'num_train_epochs': 1,
    'per_device_train_batch_size': 1,
    'gradient_accumulation_steps': 16,
    'learning_rate': 0.0002,
    'max_seq_length': 1024,
    'logging_steps': 300,
    'save_steps': 500,
    'save_total_limit': 1,
    'lr_scheduler_type': 'cosine',
    'warmup_steps': 3000,
    'lora_rank': 64,
    'lora_alpha': 16,
    'lora_dropout': 0.05,
    'gradient_checkpointing': False,
    'disable_tqdm': False,
    'optim': 'paged_adamw_32bit',
    'seed': 42,
    'fp16': True,
    'report_to': 'tensorboard',
    'dataloader_num_workers': 0,
    'save_strategy': 'steps',
    'weight_decay': 0,
    'max_grad_norm': 0.3,
    'remove_unused_columns': False
 }
```

在上面的例子中，我们修改了 `max_seq_length` 为 512,这样可以让 7B 的百川模型在消费级的 24G 显卡中即可运行微调任务。

