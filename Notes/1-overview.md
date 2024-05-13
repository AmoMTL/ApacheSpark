# Introduction

Traditionally, data flows from the HD to the RAM where it performs operations on the data. It only performs operations on the data in the RAM not the HDD.

When the size of the data gets extremely large (>1 tb), it is impractical to have 1 TB RAM, thats why we have to use clustered environment, distributed environment or parallelization so that we can distribute our data to different systems.

Ex: searching from a 100 gb excel file would take longer than if the excel file is split into 10 10gb files and searching them.

![5 vs of big data](https://www.businessprocessincubator.com/wp-content/uploads/2023/01/Infografia-5Vs-of-big-data.jpg)

1. Volume: The size of the data

2. Velocity: The speed at which the data is generated

3. Variety: Different types of data

4. Veracity: The trustworthiness of the data in terms of accuracy

5. Value: We turn the data in to useful information, i.e. create value.

## Hadoop cluster

Hadoop is java based

There are mainly three components:

1. HDFS - Hadoop Distributed File System (Not a database), a file system that shows in which format the data is saved and allows for high throughput access by partitioning the data and saving on multiple system
2. MapReduce - Compute engine

Map: It is the operation that is performed in parallel on the small portions of the dataset

Reduce: Combines all the results extracted from map

3. YARN - Resource Manager

Hadoop has a resource manager and a node manager.
![Hadoop](https://www.altexsoft.com/media/2021/06/hadoop_cluster.png)

Haddop has a master/slave architecture - all tasks come to the master node which then assigns the tasks to worker nodes depending on the location of the data

## Distributed cluster enivronment

![distributed cluster environment](https://images.ctfassets.net/xjan103pcp94/4pncjIZFAz5pKUlzwi2Agb/c6eb6957fafd8042133799b33490d4a2/blog-what-is-distributed-training-thumb.png)

## Apache spark

The MapReduce is replaced by spark, HDFS and YARN are the same. The compute engine is changed to spark.

Storage: Local/HDFS/Amazon s3
Resource manager: YARN/Spark internal resource manager/MESOS/ Kubernetes

Spark can either be deployed in distributed or standalone mode.

### Process

Source -> Ingest -> Process -> Store -> Serve data
