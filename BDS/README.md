# OCI Big Data Service (BDS)

Value position: managed open source software
- Compared to AWS EMR, BDS is less managed
	- User can master node CPU vertical scalable
  - Servermore: User can change node in os level



# [What's in the box](https://docs.oracle.com/en-us/iaas/Content/bigdata/overview.htm#odh-2.x)
- Hadoop 3.3.3
- Spark 3.2.1
- Hbase 2.4.13
- Oozie 5.2.1
- Hive 3.1.3
  - external connection is allowed only in non-ha cluster
  - port 10000 for Hive Thrift Server
- Hue 4.10.0
- Tez 0.10.2
- Sqoop 1.4.7
- Ambari 2.7.5
  - is dead
- Kafka 3.2.0
- Zookeeper 3.7.1
- JupyterHub 2.1.1
- Flume
- Flink 1.15.2
- Delta Lake 1.2.1
- Apache Ranger 2.3.0 and InfrSolr 0.1.0
- Trino 389

Base image: Oracle Linux 7.9


# Data I/O

For oracle db, [Using Big Data Connectors](https://docs.oracle.com/en-us/iaas/Content/bigdata/connectors.htm) pre-installed on BDS clusters
- BDS -> Oracle DB: Oracle Loader for Hadoop (OLH)
- Oracle DB -> BDS: Copy to Hadoop (CP2HADOOP)

For other database
- [Upload Data to HDFS and Object Storage](https://docs.oracle.com/en-us/iaas/Content/tutorials/bigdata/get-started-odh/00-overview.htm#upload)

# Limit
- Only one external metastore can be configured for a cluster
- Object Storage is used only for BDS Cloud SQL feature
- [Network specialty](./network.md) required
  - Big Data Service nodes are by default assigned private IP addresses
  - No roadmap planned to have a GUI to map public IP to private IP


