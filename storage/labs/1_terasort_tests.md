Teragen ouput :

```
[sergiosadaniowski@ip-172-31-10-186 hadoop-hdfs]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=4 10000000 terageninput
17/10/03 16:35:56 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-87.us-west-2.compute.internal/172.31.0.87:8032
17/10/03 16:35:57 INFO terasort.TeraGen: Generating 10000000 using 4
17/10/03 16:35:57 INFO mapreduce.JobSubmitter: number of splits:4
17/10/03 16:35:57 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/10/03 16:35:57 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/10/03 16:35:57 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507057975148_0001
17/10/03 16:35:58 INFO impl.YarnClientImpl: Submitted application application_1507057975148_0001
17/10/03 16:35:58 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-87.us-west-2.compute.internal:8088/proxy/application_1507057975148_0001/
17/10/03 16:35:58 INFO mapreduce.Job: Running job: job_1507057975148_0001
17/10/03 16:36:05 INFO mapreduce.Job: Job job_1507057975148_0001 running in uber mode : false
17/10/03 16:36:05 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 16:36:20 INFO mapreduce.Job:  map 25% reduce 0%
17/10/03 16:36:21 INFO mapreduce.Job:  map 100% reduce 0%
17/10/03 16:36:21 INFO mapreduce.Job: Job job_1507057975148_0001 completed successfully
17/10/03 16:36:21 INFO mapreduce.Job: Counters: 33
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=511588
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=337
		HDFS: Number of bytes written=1000000000
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters 
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=54769
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=54769
		Total vcore-milliseconds taken by all map tasks=54769
		Total megabyte-milliseconds taken by all map tasks=56083456
	Map-Reduce Framework
		Map input records=10000000
		Map output records=10000000
		Input split bytes=337
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=491
		CPU time spent (ms)=31000
		Physical memory (bytes) snapshot=1508003840
		Virtual memory (bytes) snapshot=6434336768
		Total committed heap usage (bytes)=2290089984
		Peak Map Physical memory (bytes)=388038656
		Peak Map Virtual memory (bytes)=1616904192
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=21472776955442690
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=1000000000

real	0m27.193s
user	0m5.000s
sys	0m0.282s
```




terasort output : 

```
[sergiosadaniowski@ip-172-31-10-186 hadoop-hdfs]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort  terageninput /user/sergiosadaniowski/terasortout
17/10/03 16:42:02 INFO terasort.TeraSort: starting
17/10/03 16:42:04 INFO input.FileInputFormat: Total input paths to process : 4
Spent 153ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 156ms
Sampling 10 splits of 32
Making 12 from 100000 sampled records
Computing parititions took 601ms
Spent 761ms computing partitions.
17/10/03 16:42:04 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-87.us-west-2.compute.internal/172.31.0.87:8032
17/10/03 16:42:05 INFO mapreduce.JobSubmitter: number of splits:32
17/10/03 16:42:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507057975148_0002
17/10/03 16:42:05 INFO impl.YarnClientImpl: Submitted application application_1507057975148_0002
17/10/03 16:42:05 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-87.us-west-2.compute.internal:8088/proxy/application_1507057975148_0002/
17/10/03 16:42:05 INFO mapreduce.Job: Running job: job_1507057975148_0002
17/10/03 16:42:12 INFO mapreduce.Job: Job job_1507057975148_0002 running in uber mode : false
17/10/03 16:42:12 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 16:42:26 INFO mapreduce.Job:  map 22% reduce 0%
17/10/03 16:42:27 INFO mapreduce.Job:  map 59% reduce 0%
17/10/03 16:42:28 INFO mapreduce.Job:  map 69% reduce 0%
17/10/03 16:42:29 INFO mapreduce.Job:  map 72% reduce 0%
17/10/03 16:42:34 INFO mapreduce.Job:  map 84% reduce 0%
17/10/03 16:42:35 INFO mapreduce.Job:  map 97% reduce 0%
17/10/03 16:42:36 INFO mapreduce.Job:  map 100% reduce 0%
17/10/03 16:42:43 INFO mapreduce.Job:  map 100% reduce 8%
17/10/03 16:42:45 INFO mapreduce.Job:  map 100% reduce 33%
17/10/03 16:42:46 INFO mapreduce.Job:  map 100% reduce 42%
17/10/03 16:42:50 INFO mapreduce.Job:  map 100% reduce 100%
17/10/03 16:42:51 INFO mapreduce.Job: Job job_1507057975148_0002 completed successfully
17/10/03 16:42:51 INFO mapreduce.Job: Counters: 53
	File System Counters
		FILE: Number of bytes read=439894977
		FILE: Number of bytes written=879663450
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1000005344
		HDFS: Number of bytes written=1000000000
		HDFS: Number of read operations=132
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=24
	Job Counters 
		Launched map tasks=32
		Launched reduce tasks=12
		Data-local map tasks=32
		Total time spent by all maps in occupied slots (ms)=335165
		Total time spent by all reduces in occupied slots (ms)=134773
		Total time spent by all map tasks (ms)=335165
		Total time spent by all reduce tasks (ms)=134773
		Total vcore-milliseconds taken by all map tasks=335165
		Total vcore-milliseconds taken by all reduce tasks=134773
		Total megabyte-milliseconds taken by all map tasks=343208960
		Total megabyte-milliseconds taken by all reduce tasks=138007552
	Map-Reduce Framework
		Map input records=10000000
		Map output records=10000000
		Map output bytes=1020000000
		Map output materialized bytes=434072693
		Input split bytes=5344
		Combine input records=0
		Combine output records=0
		Reduce input groups=10000000
		Reduce shuffle bytes=434072693
		Reduce input records=10000000
		Reduce output records=10000000
		Spilled Records=20000000
		Shuffled Maps =384
		Failed Shuffles=0
		Merged Map outputs=384
		GC time elapsed (ms)=5353
		CPU time spent (ms)=198340
		Physical memory (bytes) snapshot=20783058944
		Virtual memory (bytes) snapshot=70732214272
		Total committed heap usage (bytes)=24357371904
		Peak Map Physical memory (bytes)=531156992
		Peak Map Virtual memory (bytes)=1616609280
		Peak Reduce Physical memory (bytes)=383168512
		Peak Reduce Virtual memory (bytes)=1627799552
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=1000000000
	File Output Format Counters 
		Bytes Written=1000000000
17/10/03 16:42:51 INFO terasort.TeraSort: done

real	0m49.873s
user	0m7.361s
sys	0m0.344s
```