# OCI Big Data Service (BDS)

Value position: managed open source software


What's in the box
- Hadoop 3.1.2
- Spark + HistoryServer 3.0.2
- Hbase 2.2.6
- Oozie 5.2.0
- Hive 3.1.2
  - external connection is allowed only in non-ha cluster
  - port 10000 for Hive Thrift Server
- Hue
- Tez 0.10.0
- Sqoop 1.4.7
- Ambari 2.7.5
- Zookeeper 3.4.14
- Presto (preconfigured in Big Data clusters, can be managed through Ambari)
  - Use cases: ad hoc query
- JupyterHub
- Flume
- Flink (To be GA)
- Delta (To be GA)
- Apache Range




# Data I/O

For oracle db, [Using Big Data Connectors](https://docs.oracle.com/en-us/iaas/Content/bigdata/connectors.htm) pre-installed on BDS clusters
- BDS -> Oracle DB: Oracle Loader for Hadoop (OLH)
- Oracle DB -> BDS: Copy to Hadoop (CP2HADOOP)

For other database
- [Upload Data to HDFS and Object Storage](https://docs.oracle.com/en-us/iaas/Content/tutorials/bigdata/get-started-odh/00-overview.htm#upload)

# Limit
- Only one external metastore can be configured for a cluster
- Object Storage is used only for BDS Cloud SQL feature
- No plan to have a GUI to map public IP to private IP


