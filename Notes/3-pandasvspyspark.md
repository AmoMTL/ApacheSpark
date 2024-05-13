# Pandas Vs PySpark

## PySpark

Apache Spark community released a tool called PySpark compbining python and spark. Pyspark is the python API written in python to support Apache Spark.

It lets us use the power of Apache spark in order to tame big data. It is achieved by making use of the library Py4J. Using PySpark, we can work with RDD's in pytho programming language.

## Difference between PySpark and pandas

![difference](https://miro.medium.com/v2/resize:fit:1400/1*eo9rDC-kvAxCtP1dE5iZdg.png)

## Resilient Distributed Dataset (RDD)

* It is the fundamental unit of Spark/PySpark
    
    **Resilient**: It is fault tolerant and is capable of rebuilding data on failure.
    
    **Distributed**: Data is distributed among the multiple nodes of a cluster.

    **Datset**: Collection of partitioned data with values.

* Immutable and follows lazy transformation.
* These are the elements that run and operate on multiple nodes to do parallel processing on the cluster.
* You can apply multiple operation on these RDD's to achieve a certain task.
* Spark RDD can also be cached and manually partitioned.
* Operations that can be done on an RDD:
    
    **Transformation**: to create a new RDD (e.g. Filter, groupBy and map)
    
    **Action**: Instructs Spark to perform computation and send the results back to the driver.

![RDD](https://image.slidesharecdn.com/youtubespk-141216130447-conversion-gate02/95/apache-spark-rdd-101-3-638.jpg)

![process](https://www.tutorialspoint.com/apache_spark/images/iterative_operations_on_spark_rdd.jpg)

![master driver nodes](https://miro.medium.com/v2/resize:fit:1152/1*l2MUHFvWfcdiUbh7Y-fM5Q.png)

## Features of RDD

1. In-memory computation: It  stores intermediate results in distributed memory (RAM) instead of stable storage (disk).
2. Lazy evaluations: All transformations in Apache Spark are lazy, in that they do not compute theur results right away.
3. Fault tolerance: Spark RDD's are fault tolerant as they track data lineage information to rebuild lost data automatically on failure.
4. Immutability: Data is safe to share across various processes. It can also be created or retrieved anytime which makes caching, sharing and replication easy. Thus, it is a way to reach consistency in computations.
5. Persistance: Users can state which RDD's they will reuse and choose a storage strategy for them (for e.g., in-memory storage or disk).
6. Partitioning: Partitioning is the fundamental unit of parallelism in Spark RDD. Each partition is one logical division of data which is mutable. One car create a partition through some transformations on existing partitions.
7. Coarse-grained operations: It applies to all elements in datasets through maps or filter or grou by operation.
8. Location-Stickiness: RDD's are capableof defining placement preference to compute partitions. Placement preference referes to information aboutt he location of RDD. The DAGScheduler places the partitions in such a way that task is close to data as much as possible. Thus, speed up computation.