
```

time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=12 -Dmapreduce.map.memory.mb=512 65536000 tgen


```



```

[saturn@ip-172-31-38-137 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=12 -Dmapreduce.map.memory.mb=512 65536000 tgen
17/10/06 09:46:09 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-139.us-west-2.compute.internal/172.31.14.139:8032
17/10/06 09:46:10 INFO terasort.TeraSort: Generating 65536000 using 12
17/10/06 09:46:10 INFO mapreduce.JobSubmitter: number of splits:12
17/10/06 09:46:10 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/10/06 09:46:10 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/10/06 09:46:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507294882830_0001
17/10/06 09:46:10 INFO impl.YarnClientImpl: Submitted application application_1507294882830_0001
17/10/06 09:46:10 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-139.us-west-2.compute.internal:8088/proxy/application_1507294882830_0001/
17/10/06 09:46:10 INFO mapreduce.Job: Running job: job_1507294882830_0001
17/10/06 09:46:17 INFO mapreduce.Job: Job job_1507294882830_0001 running in uber mode : false
17/10/06 09:46:17 INFO mapreduce.Job:  map 0% reduce 0%
17/10/06 09:46:29 INFO mapreduce.Job:  map 2% reduce 0%
17/10/06 09:46:30 INFO mapreduce.Job:  map 12% reduce 0%
17/10/06 09:46:31 INFO mapreduce.Job:  map 15% reduce 0%
17/10/06 09:46:32 INFO mapreduce.Job:  map 19% reduce 0%
17/10/06 09:46:33 INFO mapreduce.Job:  map 23% reduce 0%
17/10/06 09:46:34 INFO mapreduce.Job:  map 24% reduce 0%
17/10/06 09:46:35 INFO mapreduce.Job:  map 27% reduce 0%
17/10/06 09:46:36 INFO mapreduce.Job:  map 31% reduce 0%
17/10/06 09:46:38 INFO mapreduce.Job:  map 34% reduce 0%
17/10/06 09:46:39 INFO mapreduce.Job:  map 38% reduce 0%
17/10/06 09:46:40 INFO mapreduce.Job:  map 39% reduce 0%
17/10/06 09:46:41 INFO mapreduce.Job:  map 42% reduce 0%
17/10/06 09:46:42 INFO mapreduce.Job:  map 44% reduce 0%
17/10/06 09:46:43 INFO mapreduce.Job:  map 45% reduce 0%
17/10/06 09:46:44 INFO mapreduce.Job:  map 46% reduce 0%
17/10/06 09:46:45 INFO mapreduce.Job:  map 48% reduce 0%
17/10/06 09:46:47 INFO mapreduce.Job:  map 49% reduce 0%
17/10/06 09:46:48 INFO mapreduce.Job:  map 51% reduce 0%
17/10/06 09:46:50 INFO mapreduce.Job:  map 52% reduce 0%
17/10/06 09:46:51 INFO mapreduce.Job:  map 53% reduce 0%
17/10/06 09:46:57 INFO mapreduce.Job:  map 54% reduce 0%
17/10/06 09:46:59 INFO mapreduce.Job:  map 57% reduce 0%
17/10/06 09:47:03 INFO mapreduce.Job:  map 60% reduce 0%
17/10/06 09:47:08 INFO mapreduce.Job:  map 61% reduce 0%
17/10/06 09:47:09 INFO mapreduce.Job:  map 62% reduce 0%
17/10/06 09:47:14 INFO mapreduce.Job:  map 64% reduce 0%
17/10/06 09:47:15 INFO mapreduce.Job:  map 67% reduce 0%
17/10/06 09:47:17 INFO mapreduce.Job:  map 69% reduce 0%
17/10/06 09:47:18 INFO mapreduce.Job:  map 71% reduce 0%
17/10/06 09:47:20 INFO mapreduce.Job:  map 72% reduce 0%
17/10/06 09:47:21 INFO mapreduce.Job:  map 74% reduce 0%
17/10/06 09:47:23 INFO mapreduce.Job:  map 75% reduce 0%
17/10/06 09:47:24 INFO mapreduce.Job:  map 76% reduce 0%
17/10/06 09:47:27 INFO mapreduce.Job:  map 77% reduce 0%
17/10/06 09:47:29 INFO mapreduce.Job:  map 78% reduce 0%
17/10/06 09:47:30 INFO mapreduce.Job:  map 79% reduce 0%
17/10/06 09:47:32 INFO mapreduce.Job:  map 80% reduce 0%
17/10/06 09:47:33 INFO mapreduce.Job:  map 82% reduce 0%
17/10/06 09:47:35 INFO mapreduce.Job:  map 84% reduce 0%
17/10/06 09:47:41 INFO mapreduce.Job:  map 86% reduce 0%
17/10/06 09:47:42 INFO mapreduce.Job:  map 88% reduce 0%
17/10/06 09:47:44 INFO mapreduce.Job:  map 89% reduce 0%
17/10/06 09:47:45 INFO mapreduce.Job:  map 91% reduce 0%
17/10/06 09:47:47 INFO mapreduce.Job:  map 92% reduce 0%
17/10/06 09:47:48 INFO mapreduce.Job:  map 93% reduce 0%
17/10/06 09:47:49 INFO mapreduce.Job:  map 94% reduce 0%
17/10/06 09:47:50 INFO mapreduce.Job:  map 95% reduce 0%
17/10/06 09:47:53 INFO mapreduce.Job:  map 98% reduce 0%
17/10/06 09:47:54 INFO mapreduce.Job:  map 99% reduce 0%
17/10/06 09:47:55 INFO mapreduce.Job:  map 100% reduce 0%
17/10/06 09:47:55 INFO mapreduce.Job: Job job_1507294882830_0001 completed successfully
17/10/06 09:47:55 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1484822
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1025
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=48
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=24
	Job Counters 
		Launched map tasks=12
		Other local map tasks=12
		Total time spent by all maps in occupied slots (ms)=1099662
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=1099662
		Total vcore-seconds taken by all map tasks=1099662
		Total megabyte-seconds taken by all map tasks=1126053888
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=1025
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2173
		CPU time spent (ms)=144260
		Physical memory (bytes) snapshot=2334220288
		Virtual memory (bytes) snapshot=13837750272
		Total committed heap usage (bytes)=4410834944
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000

real	1m48.802s
user	0m4.948s
sys	0m0.277s



```



```

[ec2-user@ip-172-31-38-137 ~]$   sudo -u hdfs hdfs dfs -ls /user/saturn/tgen
Found 13 items
-rw-r--r--   3 saturn supergroup          0 2017-10-06 09:47 /user/saturn/tgen/_SUCCESS
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:47 /user/saturn/tgen/part-m-00000
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00001
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00002
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:47 /user/saturn/tgen/part-m-00003
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00004
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00005
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:47 /user/saturn/tgen/part-m-00006
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00007
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00008
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:47 /user/saturn/tgen/part-m-00009
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00010
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:47 /user/saturn/tgen/part-m-00011
[ec2-user@ip-172-31-38-137 ~]$ 



```





