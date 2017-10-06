```

[ec2-user@ip-172-31-4-34 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 10 100
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
17/10/06 12:38:27 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-139.us-west-2.compute.internal/172.31.14.139:8032
17/10/06 12:38:27 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307907530, maxDate=1507912707530, sequenceNumber=15, masterKeyId=4 on 172.31.14.139:8020
17/10/06 12:38:27 INFO security.TokenCache: Got dt for hdfs://ip-172-31-14-139.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307907530, maxDate=1507912707530, sequenceNumber=15, masterKeyId=4)
17/10/06 12:38:27 INFO input.FileInputFormat: Total input paths to process : 10
17/10/06 12:38:27 INFO mapreduce.JobSubmitter: number of splits:10
17/10/06 12:38:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507303774544_0009
17/10/06 12:38:27 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307907530, maxDate=1507912707530, sequenceNumber=15, masterKeyId=4)
17/10/06 12:38:28 INFO impl.YarnClientImpl: Submitted application application_1507303774544_0009
17/10/06 12:38:28 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-139.us-west-2.compute.internal:8088/proxy/application_1507303774544_0009/
17/10/06 12:38:28 INFO mapreduce.Job: Running job: job_1507303774544_0009
17/10/06 12:38:37 INFO mapreduce.Job: Job job_1507303774544_0009 running in uber mode : false
17/10/06 12:38:37 INFO mapreduce.Job:  map 0% reduce 0%
17/10/06 12:38:44 INFO mapreduce.Job:  map 10% reduce 0%
17/10/06 12:38:47 INFO mapreduce.Job:  map 50% reduce 0%
17/10/06 12:38:49 INFO mapreduce.Job:  map 100% reduce 0%
17/10/06 12:38:56 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_r_000000_0, Status : FAILED
Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#8
	at org.apache.hadoop.mapreduce.task.reduce.Shuffle.run(Shuffle.java:134)
	at org.apache.hadoop.mapred.ReduceTask.run(ReduceTask.java:376)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1920)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Exceeded MAX_FAILED_UNIQUE_FETCHES; bailing-out.
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.checkReducerHealth(ShuffleSchedulerImpl.java:392)
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.copyFailed(ShuffleSchedulerImpl.java:307)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.copyFromHost(Fetcher.java:366)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.run(Fetcher.java:198)

17/10/06 12:39:04 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_r_000000_1, Status : FAILED
Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#10
	at org.apache.hadoop.mapreduce.task.reduce.Shuffle.run(Shuffle.java:134)
	at org.apache.hadoop.mapred.ReduceTask.run(ReduceTask.java:376)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1920)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Exceeded MAX_FAILED_UNIQUE_FETCHES; bailing-out.
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.checkReducerHealth(ShuffleSchedulerImpl.java:392)
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.copyFailed(ShuffleSchedulerImpl.java:307)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.copyFromHost(Fetcher.java:366)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.run(Fetcher.java:198)

17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000000_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000009_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000004_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000005_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000006_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_m_000007_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0009_r_000000_2 from host ip-172-31-4-34.us-west-2.compute.internal
17/10/06 12:39:12 INFO mapreduce.Job: Task Id : attempt_1507303774544_0009_r_000000_2, Status : FAILED
Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#7
	at org.apache.hadoop.mapreduce.task.reduce.Shuffle.run(Shuffle.java:134)
	at org.apache.hadoop.mapred.ReduceTask.run(ReduceTask.java:376)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1920)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Exceeded MAX_FAILED_UNIQUE_FETCHES; bailing-out.
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.checkReducerHealth(ShuffleSchedulerImpl.java:392)
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.copyFailed(ShuffleSchedulerImpl.java:307)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.copyFromHost(Fetcher.java:366)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.run(Fetcher.java:198)

17/10/06 12:39:13 INFO mapreduce.Job:  map 40% reduce 0%
^C
real	0m52.657s
user	0m5.165s
sys	0m0.303s
[ec2-user@ip-172-31-4-34 ~]$ 



```