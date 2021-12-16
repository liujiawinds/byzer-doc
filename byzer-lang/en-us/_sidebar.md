- Byzer-Lang Introduction
  * [Byzer-Lang](/byzer-lang/en-us/introduction/kolo_lang_intro.md)
  * [Online Trial](/byzer-lang/en-us/introduction/byzer_lab.md)
  * [Get Started](/byzer-lang/en-us/introduction/get_started.md)
  * [FAQ](/byzer-lang/en-us/appendix/faq.md)
  * [How to Contribute](/byzer-lang/en-us/appendix/contribute.md)  

- What's New
  * [New Features](/byzer-lang/en-us/what's_new/new_features.md)

- Installation
  * [Byzer Engine](/byzer-lang/en-us/installation/kolo_engine.md)
  * [Byzer Desktop](/byzer-lang/en-us/installation/kolo_desktop.md)    
  * [Byzer CLI](/byzer-lang/en-us/installation/kolo_cli.md)
  * [Byzer Sandbox](/byzer-lang/en-us/installation/sandbox.md)

- Byzer-lang Grammar Manual
  * [Byzer-Lang Guide](/byzer-lang/en-us/grammar/outline.md)  
  * [Data Load/Load](/byzer-lang/en-us/grammar/load.md)
  * [Data Transform/Select](/byzer-lang/en-us/grammar/select.md)
  * [Data Save/Save](/byzer-lang/en-us/grammar/save.md)
  * [Extension/Train|Run|Predict](/byzer-lang/en-us/grammar/et_statement.md)
  * [Model,UDF Register/Register](/byzer-lang/en-us/grammar/register.md)  
  * [Variable/Set](/byzer-lang/en-us/grammar/set.md)
  * [Macro Function](/byzer-lang/en-us/grammar/macro.md)
  * [Code Import/Include](/byzer-lang/en-us/grammar/include.md)
  * [Branch/If|Else](/byzer-lang/en-us/grammar/branch_statement.md)
  * [Build-in Marco Functions](/byzer-lang/en-us/grammar/commands.md)

- Data Pipeline & Analysis
    - Load Datasource in Byzer
      * [Datasource](/byzer-lang/en-us/datasource/README.md)
      * [RestAPI](/byzer-lang/en-us/datasource/restapi.md)
      * [JDBC](/byzer-lang/en-us/datasource/jdbc.md)
      * [ElasticSearch](/byzer-lang/en-us/datasource/es.md)
      * [Solr](/byzer-lang/en-us/datasource/solr.md)
      * [HBase](/byzer-lang/en-us/datasource/hbase.md)
      * [MongoDB](/byzer-lang/en-us/datasource/mongodb.md)
      * [Parquet/Json/Text/Xml/Csv](/byzer-lang/en-us/datasource/file.md)
      * [jsonStr/script/ByzerAPI/ByzerConf](/byzer-lang/en-us/datasource/kolo_source.md)
      * [Kafka](/byzer-lang/en-us/datasource/kafka.md)
      * [MockStreaming](/byzer-lang/en-us/datasource/mock_streaming.md)

    - Data Warehouse / DataLake
        * [Data Warehouse / DataLake](/byzer-lang/en-us/datahouse/README.md)
        * [Load/Save in Hive](/byzer-lang/en-us/datahouse/hive.md)
        * [Delta lake](/byzer-lang/en-us/datahouse/delta_lake.md)
        * [MySQL Binlog](/byzer-lang/en-us/datahouse/mysql_binlog.md)

    - Extend with Python 
        * [Use Python to Extend Byzer](/byzer-lang/en-us/python/README.md)
        * [Environment](/byzer-lang/en-us/python/env.md)
        * [ETL](/byzer-lang/en-us/python/etl.md)
        * [Train](/byzer-lang/en-us/python/train.md)
        * [PyJava API Introduction](/byzer-lang/en-us/python/pyjava.md)
        * [Read Excel](/byzer-lang/en-us/python/read_excel.md)
        * [Write Excel](/byzer-lang/en-us/python/write_excel.md)
        * [Resource Restriction under K8S](/byzer-lang/en-us/python/k8s_resource.md)
        * [Datamode](/byzer-lang/en-us/python/datamode.md)
        * [Parallel in Python](/byzer-lang/en-us/python/py_parallel.md)

    * UDF Extension
        * [UDF in Byzer](/byzer-lang/en-us/udf/README.md)
        * [Built-In UDF](/byzer-lang/en-us/udf/built_in_udf/README.md)
          * [Http request](/byzer-lang/en-us/udf/built_in_udf/http.md)
          * [Common Functions](/byzer-lang/en-us/udf/built_in_udf/vec.md)
        * [Extend UDF](/byzer-lang/en-us/udf/extend_udf/README.md)
          * [Python UDF](/byzer-lang/en-us/udf/extend_udf/python_udf.md)
          * [Scala UDF](/byzer-lang/en-us/udf/extend_udf/scala_udf.md)
          * [Scala UDAF](/byzer-lang/en-us/udf/extend_udf/scala_udaf.md)
          * [Java UDF](/byzer-lang/en-us/udf/extend_udf/java_udf.md)

    * Streaming Processing
      * [Streaming Process](/byzer-lang/en-us/streaming/README.md)
      * [Byzer Kafka Tools](/byzer-lang/en-us/streaming/kafka_tool.md)
      * [Query from Kafka](/byzer-lang/en-us/streaming/query_kafka.md)
      * [Set Callback](/byzer-lang/en-us/streaming/callback.md)
      * [Save Result in Batch Mode](/byzer-lang/en-us/streaming/save_in_batch.md)
      * [Use window/watermark](/byzer-lang/en-us/streaming/window_watermark.md)
      * [Update MySQL data in stream](/byzer-lang/en-us/streaming/stream_update_mysql.md)

- Machine Learning
    * [Feature Engineering](/byzer-lang/en-us/ml/feature/README.md)
        * [NLP](/byzer-lang/en-us/ml/feature/nlp/README.md)
            * [TFIDF](/byzer-lang/en-us/ml/feature/nlp/tfidf.md)
            * [Word2Vec](/byzer-lang/en-us/ml/feature/nlp/word2vec.md)
        * [Feature Scaling](/byzer-lang/en-us/ml/feature/scale.md)
        * [Normalization](/byzer-lang/en-us/ml/feature/normalize.md)
        * [Confusion Matrix](/byzer-lang/en-us/ml/feature/confusion_matrix.md)
        * [Discretization](/byzer-lang/en-us/ml/feature/discretizer/README.md)
            * [Bucketizer](/byzer-lang/en-us/ml/feature/discretizer/bucketizer.md)
            * [Quantile](/byzer-lang/en-us/ml/feature/discretizer/quantile.md)
        * [Map to Vector](/byzer-lang/en-us/ml/feature/vecmap.md)
        * [Data Split](/byzer-lang/en-us/ml/feature/rate_sample.md)

    * [Built-In Algorithms](/byzer-lang/en-us/ml/algs/README.md)
        * [AutoML](/byzer-lang/en-us/ml/algs/auto_ml.md) 
        * [KMeans](/byzer-lang/en-us/ml/algs/kmeans.md)
        * [NaiveBayes](/byzer-lang/en-us/ml/algs/naive_bayes.md)
        * [ALS](/byzer-lang/en-us/ml/algs/als.md)
        * [RandomForest](/byzer-lang/en-us/ml/algs/random_forest.md) 
        * [LogisticRegression](/byzer-lang/en-us/ml/algs/logistic_regression.md)
        * [LinearRegression](/byzer-lang/en-us/ml/algs/linear_regression.md)
        * [LDA](/byzer-lang/en-us/ml/algs/lda.md)

    * [Deploy Algorithm as API Service](/byzer-lang/en-us/ml/api_service/README.md)
        * [Design and Principles](/byzer-lang/en-us/ml/api_service/design.md)
        * [Deploy Process](/byzer-lang/en-us/ml/api_service/process.md)

- Deep Learning
    * [Integration with Java DL Framework](/byzer-lang/en-us/dl/README.md)
        * [Load Images](/byzer-lang/en-us/dl/load_image.md)
        * [Cifar10 Example](/byzer-lang/en-us/dl/cifar10.md)
        

- Extension
    * [Extension Introduction](/byzer-lang/en-us/extension/README.md)
        * [Extension Store](/byzer-lang/en-us/extension/installation/store.md)
        * [Online Install](/byzer-lang/en-us/extension/installation/online_install.md)
        * [Offline Install](/byzer-lang/en-us/extension/installation/offline_install.md)
    * [Estimator-Transformer](/byzer-lang/en-us/extension/et/README.md)
    * [DataSource Extension](/byzer-lang/en-us/extension/datasource/README.md)
        * [Excel](/byzer-lang/en-us/extension/datasource/excel.md)
        * [HBase](/byzer-lang/en-us/extension/datasource/hbase.md)


- Security 
    * [Interface ACL](/byzer-lang/en-us/security/interface_acl/README.md)
    * [Data ACL](/byzer-lang/en-us/security/data_acl/README.md)

- Development
    * Dev Environment
      * [Dev Environment](/byzer-lang/en-us/developer/dev_env/README.md)
      * [Spark 2.4.3 Env](/byzer-lang/en-us/developer/dev_env/spark_2_4_3.md)
      * [Spark 3.0.0 Env](/byzer-lang/en-us/developer/dev_env/spark_3_0_0.md)    
    * Extension Development
      * [ET Development](/byzer-lang/en-us/developer/extension/et_dev.md)
      * [Datasource Extension Development](/byzer-lang/en-us/developer/extension/ds_dev.md)
    * [Integration Test](/byzer-lang/en-us/developer/it/integration_test.md)     
    * API
      * [Byzer Engine Rest API](/byzer-lang/en-us/developer/api/README.md)
        * [Script Run API](/byzer-lang/en-us/developer/api/run_script_api.md)
        * [Code Suggestion API](/byzer-lang/en-us/developer/api/code_suggest.md)
      * [Liveness API](/byzer-lang/en-us/developer/api/liveness.md)
      * [Readness API](/byzer-lang/en-us/developer/api/readiness.md)
    * [Performance Tunning](/byzer-lang/en-us/developer/tunning/dynamic_resource.md)


- Appendix
    * Release
      * [Byzer Version Management](/byzer-lang/en-us/appendix/release-notes/version.md)
      * [Byzer 2.2.0](/byzer-lang/en-us/appendix/release-notes/2.2.0.md)
      * [MLSQL Stack 2.1.0](/byzer-lang/en-us/appendix/release-notes/2.1.0.md)
      * [MLSQL Stack 2.0.1](/byzer-lang/en-us/appendix/release-notes/2.0.1.md)
      * [MLSQL Stack 2.0.0](/byzer-lang/en-us/appendix/release-notes/2.0.0.md)
    * [Terms](/byzer-lang/en-us/appendix/terms.md)  
    * [Blog](/byzer-lang/en-us/appendix/blog.md)   

