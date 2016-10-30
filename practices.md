# Practice 1 notes

hadoop fs -ls /user

    [cloudera@quickstart]~/Desktop/datasets% hadoop fs -ls /user
    Found 9 items
    drwxr-xr-x   - cloudera cloudera            0 2016-10-19 14:27 /user/cloudera
    drwxr-xr-x   - hdfs     supergroup          0 2016-10-17 15:28 /user/hdfs
    drwxr-xr-x   - mapred   hadoop              0 2016-08-10 13:07 /user/history
    drwxrwxrwx   - hive     supergroup          0 2016-08-10 13:09 /user/hive
    drwxrwxrwx   - hue      supergroup          0 2016-08-10 13:08 /user/hue
    drwxrwxrwx   - jenkins  supergroup          0 2016-08-10 13:07 /user/jenkins
    drwxrwxrwx   - oozie    supergroup          0 2016-08-10 13:08 /user/oozie
    drwxrwxrwx   - root     supergroup          0 2016-10-19 14:24 /user/root
    drwxr-xr-x   - hdfs     supergroup          0 2016-08-10 13:09 /user/spark


- datasets is under `/home/cloudera/Desktop/datasets` not `~`


move sample data from local to HDFS

- cd /home/cloudera/Desktop/datasets
- hadoop fs -put stock-sample /user/cloudera/ 



[cloudera@quickstart]~/Desktop/datasets% hadoop fs -cat stock-sample/stock-sample/BOX | tail -n 5
2015-01-29,19.90,19.950001,18.51,18.799999,3419500,18.799999
2015-01-28,21.620001,21.84,19.60,19.780001,5047400,19.780001
2015-01-27,22.00,22.469999,21.17,21.299999,3272500,21.299999
2015-01-26,23.67,24.389999,22.50,22.60,8677200,22.60
2015-01-23,20.200001,24.73,20.16,23.23,42593200,23.23


Remove a directory  `hadoop fs -rm -r stock-sample/`


# Practice 2 notes




    [cloudera@quickstart]~/shared_workspace/workspace/practice_2/target% hadoop jar ./practice_2OLD-1.0.0-SNAPSHOT.jar wordcount.MR2WordCount shakespeare/comedies ./lala

    - shakespeare/comedies : HDFS path
    - ./lala : HDFS path


    1 : shakespeare/comedies2 : ./lala16/10/27 16:41:00 INFO client.RMProxy: Connecting to ResourceManager at /0.0.0.0:8032
    16/10/27 16:41:01 WARN mapreduce.JobResourceUploader: Hadoop command-line option parsing not performed. Implement the Tool interface and execute your application with ToolRunner to remedy this.
    16/10/27 16:41:02 INFO input.FileInputFormat: Total input paths to process : 17
    16/10/27 16:41:02 INFO mapreduce.JobSubmitter: number of splits:17
    16/10/27 16:41:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1477503273913_0002
    16/10/27 16:41:03 INFO impl.YarnClientImpl: Submitted application application_1477503273913_0002
    16/10/27 16:41:03 INFO mapreduce.Job: The url to track the job: http://quickstart.cloudera:8088/proxy/application_1477503273913_0002/
    16/10/27 16:41:03 INFO mapreduce.Job: Running job: job_1477503273913_0002
    16/10/27 16:41:18 INFO mapreduce.Job: Job job_1477503273913_0002 running in uber mode : false
    16/10/27 16:41:18 INFO mapreduce.Job:  map 0% reduce 0%
