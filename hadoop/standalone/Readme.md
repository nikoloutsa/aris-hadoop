# Standalone Operation

This script describes how to set up and configure a single-node Hadoop installation so that you can quickly perform simple operations using Hadoop MapReduce and the Hadoop Distributed File System (HDFS).

Hadoop is configure to run in a non-distributed mode, as a single Java process. This is useful for debugging.

## Example 

The following example copies the unpacked conf directory to use as input and then finds and displays every match of the given regular expression. Output is written to the given output directory.

```
INPUT="${WORK}/input"
mkdir -p ${INPUT}
cp ${HADOOP_HOME}/etc/hadoop/* ${INPUT} 

OUTPUT="${WORK}/output"

hadoop jar ${HADOOP_HOME}/share/hadoop/mapreduce/hadoop-mapreduce-examples-*.jar grep ${INPUT} ${OUTPUT} 'dfs[a-z.]+'

cat ${OUTPUT}/*
```

### Submit SLURM script

Run example 
```
sbatch hadoop.run
```

### Results

Result will list all the matches in all the input files.

```
cat hadoop.out
```

```
6	dfs.audit.logger
4	dfs.class
3	dfs.server.namenode.
2	dfs.period
2	dfs.audit.log.maxfilesize
2	dfs.audit.log.maxbackupindex
1	dfsmetrics.log
1	dfsadmin
1	dfs.servers
1	dfs.file
```
