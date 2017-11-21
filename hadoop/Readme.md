# ARIS HADOOP TEST CONFIGURATION

This document describes how to configure Hadoop so that you can perform Hadoop MapReduce and
Hadoop Distributed File System (HDFS) operations on ARIS supercomputer.

The Apache Hadoop software library is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models.

To run Hadoop on ARIS supercomputer we start up a Hadoop cluster each time a Hadoop job is submitted.

## Modules

```
module load java/1.7.0
module load hadoop/2.7.2
```

## Example
The following example copies the unpacked conf directory to use as input and then finds and displays every match of the given regular expression. Output is written to the given output directory.

### Run

```
sbatch hadoop.run
```

### Output

Result will list all the matches in all the input files.

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
