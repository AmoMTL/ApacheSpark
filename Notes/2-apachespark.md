# Apache Spark / PySpark

Invented by 2009 and founded Databricks in 2013, it is written in Scala - it is a lightning fast real-time processing framework.

For python interface Py4J library is used

Spark has advanced features such as in-memory computations, lazy execution and parallel processing

## In-memory computations
In spark, the data is stored in the RAM, making computations 100 times faster than hadoop, where the data is stored in HDD transferred to RAM where the computation takes place and then transferred back to the HDD

![hadoop vs spark](https://www.researchgate.net/profile/Hamid-Mushtaq/publication/319284382/figure/fig1/AS:531456718245888@1503720563930/Spark-vs-Hadoop-MapReduce.png)

## Lazy Execution

In spark, unless an operation on a data needs to be performed the data is not stored in the RAM

## Parallel processing

Distributing the workload to different nodes (similar to hadoop).

## Summary 

Apache Hadoop MapReduce was performing batch processing only and lacked real-time processing feature. Spark does Batch adn real-time processing.

Hadoop is the complete package - it has the storage system, compute engine (MapReduce) and resource manager. Spark is just the compute engine.

Hadoop is disk oriented and spark is memory oriented.

