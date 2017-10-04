[ec2-user@ip-172-31-0-35 process]$ beeline 
Beeline version 1.1.0-cdh5.11.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-35.us-west-2.compute.internal@AGNOSTIC.COM
scan complete in 1ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-0-35.us-west-2.compute.internal@AGNOSTIC.COM
Connected to: Apache Hive (version 1.1.0-cdh5.11.0)
Driver: Hive JDBC (version 1.1.0-cdh5.11.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171004160202_250bd191-906d-446a-9c89-cc78992ab654): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004160202_250bd191-906d-446a-9c89-cc78992ab654); Time taken: 0.652 seconds
INFO  : Executing command(queryId=hive_20171004160202_250bd191-906d-446a-9c89-cc78992ab654): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004160202_250bd191-906d-446a-9c89-cc78992ab654); Time taken: 0.247 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.248 seconds)
0: jdbc:hive2://localhost:10000/default> 
