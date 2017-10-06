```
ec2-user@ip-172-31-4-34 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort  /user/saturn/tgen /user/saturn/tsort
17/10/06 12:21:09 INFO terasort.TeraSort: starting
17/10/06 12:21:11 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507306871486, maxDate=1507911671486, sequenceNumber=13, masterKeyId=4 on 172.31.14.139:8020
17/10/06 12:21:11 INFO security.TokenCache: Got dt for hdfs://ip-172-31-14-139.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507306871486, maxDate=1507911671486, sequenceNumber=13, masterKeyId=4)
17/10/06 12:21:11 INFO input.FileInputFormat: Total input paths to process : 12
Spent 319ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 324ms
Sampling 10 splits of 204
Making 12 from 100000 sampled records
Computing parititions took 601ms
Spent 927ms computing partitions.
17/10/06 12:21:12 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-139.us-west-2.compute.internal/172.31.14.139:8032
17/10/06 12:21:12 INFO mapreduce.JobSubmitter: number of splits:204
17/10/06 12:21:12 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507303774544_0007
17/10/06 12:21:12 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507306871486, maxDate=1507911671486, sequenceNumber=13, masterKeyId=4)
17/10/06 12:21:13 INFO impl.YarnClientImpl: Submitted application application_1507303774544_0007
17/10/06 12:21:13 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-139.us-west-2.compute.internal:8088/proxy/application_1507303774544_0007/
17/10/06 12:21:13 INFO mapreduce.Job: Running job: job_1507303774544_0007
17/10/06 12:21:21 INFO mapreduce.Job: Job job_1507303774544_0007 running in uber mode : false
17/10/06 12:21:21 INFO mapreduce.Job:  map 100% reduce 100%
17/10/06 12:21:22 INFO mapreduce.Job: Job job_1507303774544_0007 failed with state KILLED due to: REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
Job received Kill while in RUNNING state.
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>
REDUCE capability required is more than the supported max container capability in the cluster. Killing the Job. reduceResourceRequest: <memory:24576, vCores:1> maxContainerCapability:<memory:17034, vCores:8>

17/10/06 12:21:22 INFO mapreduce.Job: Counters: 4
	Job Counters 
		Killed map tasks=204
		Killed reduce tasks=12
		Total time spent by all maps in occupied slots (ms)=0
		Total time spent by all reduces in occupied slots (ms)=0
17/10/06 12:21:22 INFO terasort.TeraSort: done

real	0m13.677s
user	0m7.529s
sys	0m0.316s
[ec2-user@ip-172-31-4-34 ~]$ sudo nano /etc/hosts
[ec2-user@ip-172-31-4-34 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort  /user/saturn/tgen /user/saturn/tsort
17/10/06 12:30:19 INFO terasort.TeraSort: starting
17/10/06 12:30:21 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307421291, maxDate=1507912221291, sequenceNumber=14, masterKeyId=4 on 172.31.14.139:8020
17/10/06 12:30:21 INFO security.TokenCache: Got dt for hdfs://ip-172-31-14-139.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307421291, maxDate=1507912221291, sequenceNumber=14, masterKeyId=4)
17/10/06 12:30:21 INFO input.FileInputFormat: Total input paths to process : 12
Spent 314ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 320ms
Sampling 10 splits of 204
Making 12 from 100000 sampled records
Computing parititions took 578ms
Spent 901ms computing partitions.
17/10/06 12:30:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-139.us-west-2.compute.internal/172.31.14.139:8032
17/10/06 12:30:22 INFO mapreduce.JobSubmitter: number of splits:204
17/10/06 12:30:22 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507303774544_0008
17/10/06 12:30:22 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.14.139:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@SERGIOSADANIOWSKI.HQ, renewer=yarn, realUser=, issueDate=1507307421291, maxDate=1507912221291, sequenceNumber=14, masterKeyId=4)
17/10/06 12:30:22 INFO impl.YarnClientImpl: Submitted application application_1507303774544_0008
17/10/06 12:30:23 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-139.us-west-2.compute.internal:8088/proxy/application_1507303774544_0008/
17/10/06 12:30:23 INFO mapreduce.Job: Running job: job_1507303774544_0008
17/10/06 12:30:31 INFO mapreduce.Job: Job job_1507303774544_0008 running in uber mode : false
17/10/06 12:30:31 INFO mapreduce.Job:  map 0% reduce 0%
17/10/06 12:30:49 INFO mapreduce.Job:  map 3% reduce 0%
17/10/06 12:30:50 INFO mapreduce.Job:  map 4% reduce 0%
17/10/06 12:30:51 INFO mapreduce.Job:  map 11% reduce 0%
17/10/06 12:31:05 INFO mapreduce.Job:  map 12% reduce 0%
17/10/06 12:31:06 INFO mapreduce.Job:  map 14% reduce 0%
17/10/06 12:31:07 INFO mapreduce.Job:  map 15% reduce 0%
17/10/06 12:31:10 INFO mapreduce.Job:  map 22% reduce 0%
17/10/06 12:31:11 INFO mapreduce.Job:  map 23% reduce 0%
17/10/06 12:31:24 INFO mapreduce.Job:  map 26% reduce 0%
17/10/06 12:31:30 INFO mapreduce.Job:  map 34% reduce 0%
17/10/06 12:31:41 INFO mapreduce.Job:  map 37% reduce 0%
17/10/06 12:31:48 INFO mapreduce.Job:  map 38% reduce 0%
17/10/06 12:31:49 INFO mapreduce.Job:  map 45% reduce 0%
17/10/06 12:31:58 INFO mapreduce.Job:  map 46% reduce 0%
17/10/06 12:31:59 INFO mapreduce.Job:  map 49% reduce 0%
17/10/06 12:32:08 INFO mapreduce.Job:  map 56% reduce 0%
17/10/06 12:32:16 INFO mapreduce.Job:  map 60% reduce 0%
17/10/06 12:32:26 INFO mapreduce.Job:  map 61% reduce 0%
17/10/06 12:32:27 INFO mapreduce.Job:  map 67% reduce 0%
17/10/06 12:32:28 INFO mapreduce.Job:  map 68% reduce 0%
17/10/06 12:32:34 INFO mapreduce.Job:  map 71% reduce 0%
17/10/06 12:32:42 INFO mapreduce.Job:  map 73% reduce 0%
17/10/06 12:32:43 INFO mapreduce.Job:  map 75% reduce 0%
17/10/06 12:32:47 INFO mapreduce.Job:  map 79% reduce 0%
17/10/06 12:32:52 INFO mapreduce.Job:  map 82% reduce 0%
17/10/06 12:32:56 INFO mapreduce.Job:  map 85% reduce 0%
17/10/06 12:32:57 INFO mapreduce.Job:  map 86% reduce 0%
17/10/06 12:33:00 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_r_000000_0, Status : FAILED
Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#9
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

17/10/06 12:33:03 INFO mapreduce.Job:  map 87% reduce 0%
17/10/06 12:33:04 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_r_000001_0, Status : FAILED
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

17/10/06 12:33:05 INFO mapreduce.Job:  map 89% reduce 0%
17/10/06 12:33:06 INFO mapreduce.Job:  map 91% reduce 0%
17/10/06 12:33:08 INFO mapreduce.Job:  map 92% reduce 0%
17/10/06 12:33:09 INFO mapreduce.Job:  map 95% reduce 0%
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000009_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000010_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000066_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000054_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000019_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000013_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000012_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000040_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000041_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:09 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000011_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job:  map 85% reduce 0%
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000005_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000004_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000045_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000034_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000039_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000022_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000063_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000043_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000044_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:10 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_m_000042_0, Status : FAILED
Too many fetch failures. Failing the attempt. Last failure reported by attempt_1507303774544_0008_r_000000_1 from host ip-172-31-38-137.us-west-2.compute.internal
17/10/06 12:33:11 INFO mapreduce.Job: Task Id : attempt_1507303774544_0008_r_000000_1, Status : FAILED
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

17/10/06 12:33:13 INFO mapreduce.Job:  map 86% reduce 0%
^C
real	2m55.653s
user	0m8.125s
sys	0m0.384s

```