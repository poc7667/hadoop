# Part 1

## Spark part(Eclipse)

Here the input path is local FS, not HDFS

/home/cloudera/workspace/practice_2/data/shakespeare/* output_shakespeare_spark


## Spark (command line)

    % hadoop jar ./practice_2OLD-1.0.0-SNAPSHOT.jar wordcount.MR2WordCount "shakespeare/*" output_shakespeare_spark_cmd


![inline](https://i.imgur.com/1G7Tnck.png=300x "Title")

## Hadoop Part

`shakespeare/*` is the input folder under HDFS, not local file system

Run the command

- hadoop jar ./practice_2OLD-1.0.0-SNAPSHOT.jar wordcount.MR2WordCount shakespeare/* output_shakespea

Ls the result 

![inline](https://i.imgur.com/xyqelM4.png=300x "Title")

Fetch the result from HDFS

- hadoop fs -get output_shakespea_1477784199234/part-r-00004 ~/current_workspace

Process of screenshot

![inline](https://i.imgur.com/gfgCtEo.png=300x "Title")


- HUE log

![inline](https://i.imgur.com/hScXOuR.png=300x "Title")



