#Spark

## Spark Standalone Mode

Start a standalone Spark cluster.
(No web UI available)

Edit spark configuration variables: `./conf/spark-env.sh`

```
# - SPARK_CONF_DIR      Alternate conf dir. (Default: ${SPARK_HOME}/conf)
SPARK_CONF_DIR=conf
# - SPARK_LOG_DIR       Where log files are stored.  (Default: ${SPARK_HOME}/logs)
SPARK_LOG_DIR=logs
```

## Example

Submit a spark job on ARIS. To calculate PI using python and java examples.

```
sbatch spark.run
```
