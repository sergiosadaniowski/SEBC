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



george SHOW TABLES 

0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171004165252_7c25ffe6-a719-4a65-922e-ee82507b6bed): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004165252_7c25ffe6-a719-4a65-922e-ee82507b6bed); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20171004165252_7c25ffe6-a719-4a65-922e-ee82507b6bed): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004165252_7c25ffe6-a719-4a65-922e-ee82507b6bed); Time taken: 0.122 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.282 seconds)
0: jdbc:hive2://localhost:10000/default> 



fernindand show tables 

Connected to: Apache Hive (version 1.1.0-cdh5.11.0)
Driver: Hive JDBC (version 1.1.0-cdh5.11.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171004165454_13a65b66-2df4-46c2-8299-c5a683551cb6): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171004165454_13a65b66-2df4-46c2-8299-c5a683551cb6); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20171004165454_13a65b66-2df4-46c2-8299-c5a683551cb6): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171004165454_13a65b66-2df4-46c2-8299-c5a683551cb6); Time taken: 0.123 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.297 seconds)
0: jdbc:hive2://localhost:10000/default> 
