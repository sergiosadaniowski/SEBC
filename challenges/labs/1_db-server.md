

```
mysql> select @@hostname;
+-------------------------------------------+
| @@hostname                                |
+-------------------------------------------+
| ip-172-31-9-71.us-west-2.compute.internal |
+-------------------------------------------+
1 row in set (0,00 sec)

mysql> show variables where Variable_name like '%host%';
+-------------------------------+-------------------------------------------+
| Variable_name                 | Value                                     |
+-------------------------------+-------------------------------------------+
| host_cache_size               | 342                                       |
| hostname                      | ip-172-31-9-71.us-west-2.compute.internal |
| performance_schema_hosts_size | 100                                       |
| report_host                   |                                           |
+-------------------------------+-------------------------------------------+
4 rows in set (0,00 sec)

mysql> 


```


```

mysql> SHOW VARIABLES LIKE "%version%";
+-------------------------+------------------------------+
| Variable_name           | Value                        |
+-------------------------+------------------------------+
| innodb_version          | 5.6.37                       |
| protocol_version        | 10                           |
| slave_type_conversions  |                              |
| version                 | 5.6.37-log                   |
| version_comment         | MySQL Community Server (GPL) |
| version_compile_machine | x86_64                       |
| version_compile_os      | Linux                        |
+-------------------------+------------------------------+
7 rows in set (0,00 sec)

mysql> 


```


```

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
8 rows in set (0,00 sec)

mysql> 


```