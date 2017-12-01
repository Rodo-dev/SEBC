* The full teragen command and output
`HADOOP_USER_NAME=hdfs hadoop jar hadoop-examples.jar teragen -D dfs.block.size=33554432 -D mapreduce.job.maps=12 65536000 /user/saturn/results/tgen` <br>

17/12/01 19:54:05 INFO client.RMProxy: Connecting to ResourceManager at nodo1.rodo.com/10.0.1.4:8032
17/12/01 19:54:05 INFO terasort.TeraSort: Generating 65536000 using 12
17/12/01 19:54:05 INFO mapreduce.JobSubmitter: number of splits:12
17/12/01 19:54:05 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/12/01 19:54:06 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512154212415_0005
17/12/01 19:54:06 INFO impl.YarnClientImpl: Submitted application application_1512154212415_0005
17/12/01 19:54:06 INFO mapreduce.Job: The url to track the job: http://nodo1.rodo.com:8088/proxy/application_1512154212415_0005/
17/12/01 19:54:06 INFO mapreduce.Job: Running job: job_1512154212415_0005
17/12/01 19:54:11 INFO mapreduce.Job: Job job_1512154212415_0005 running in uber mode : false
17/12/01 19:54:11 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 19:54:22 INFO mapreduce.Job:  map 7% reduce 0%
17/12/01 19:54:23 INFO mapreduce.Job:  map 18% reduce 0%
17/12/01 19:54:25 INFO mapreduce.Job:  map 21% reduce 0%
17/12/01 19:54:26 INFO mapreduce.Job:  map 26% reduce 0%
17/12/01 19:54:29 INFO mapreduce.Job:  map 37% reduce 0%
17/12/01 19:54:32 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 19:54:35 INFO mapreduce.Job:  map 56% reduce 0%
17/12/01 19:54:39 INFO mapreduce.Job:  map 65% reduce 0%
17/12/01 19:54:42 INFO mapreduce.Job:  map 75% reduce 0%
17/12/01 19:54:45 INFO mapreduce.Job:  map 82% reduce 0%
17/12/01 19:54:49 INFO mapreduce.Job:  map 89% reduce 0%
17/12/01 19:54:51 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 19:54:52 INFO mapreduce.Job:  map 92% reduce 0%
17/12/01 19:54:53 INFO mapreduce.Job:  map 97% reduce 0%
17/12/01 19:54:54 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 19:54:55 INFO mapreduce.Job: Job job_1512154212415_0005 completed successfully
17/12/01 19:54:55 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1477814
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
		Total time spent by all maps in occupied slots (ms)=470020
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=470020
		Total vcore-seconds taken by all map tasks=470020
		Total megabyte-seconds taken by all map tasks=481300480
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=1025
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1495
		CPU time spent (ms)=127480
		Physical memory (bytes) snapshot=3398656000
		Virtual memory (bytes) snapshot=19137761280
		Total committed heap usage (bytes)=5739905024
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
<br>
* The command and output of hdfs dfs -ls /user/saturn/tgen
`HADOOP_USER_NAME=hdfs hdfs dfs -ls -h /user/saturn/results/tgen`
<br>
Found 13 items
-rw-r--r--   3 hdfs supergroup          0 2017-12-01 19:54 /user/saturn/results/tgen/_SUCCESS
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00000
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00001
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00002
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00003
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00004
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00005
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00006
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00007
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00008
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00009
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00010
-rw-r--r--   3 hdfs supergroup    520.8 M 2017-12-01 19:54 /user/saturn/results/tgen/part-m-00011
<br>
* The command and output of hadoop fsck -blocks /user/saturn
`HADOOP_USER_NAME=hdfs hadoop fsck -blocks /user/saturn/results`
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://nodo1.rodo.com:50070
FSCK started by hdfs (auth:SIMPLE) from /10.0.1.5 for path /user/saturn/results at Fri Dec 01 19:58:28 UTC 2017
.............Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	2
 Total files:	13
 Total symlinks:		0
 Total blocks (validated):	204 (avg. block size 32125490 B)
 Minimally replicated blocks:	204 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Dec 01 19:58:28 UTC 2017 in 9 milliseconds

The filesystem under path '/user/saturn/results' is HEALTHY

