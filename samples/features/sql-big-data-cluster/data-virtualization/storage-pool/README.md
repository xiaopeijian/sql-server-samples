# Data virtualization in SQL Server 2019 big data cluster

In SQL Server 2019 big data clusters, the SQL Server engine has gained the ability to natively read HDFS files, such as CSV and parquet files, by using SQL Server instances collocated on each of the HDFS data nodes to filter and aggregate data locally in parallel across all of the HDFS data nodes. SQL Server 2019 introduces new ODBC connectors to data sources like SQL Server, Oracle, MongoDB and Teradata.

## Query data in HDFS from SQL Server master

**Applies to: SQL Server 2019 big data cluster**

In SQL Server 2019 big data cluster, the storage pool consists of HDFS data node with SQL Server & Spark endpoints. In this example, you are going to create an external table in the SQL Server Master instance that points to data in HDFS within the SQL Server Big data cluster. You will then join the data in the external table with high value data in SQL Master instance.

### Instructions

1. Connect to HDFS/Knox gateway from Azure Data Studio using SQL Server big data cluster connection type.

1. Run the [../../spark/spark-sql.ipynb](../../spark/spark-sql.ipynb/) notebook to generate the sample parquet file(s).

1. Connect to SQL Server Master instance.

1. Execute the [web-clickstreams-hdfs-csv.sql](web-clickstreams-hdfs-csv.sql). This script demonstrates how to read CSV file(s) stored in HDFS.

1. Execute the [web-clickstreams-parquet.sql](web-clickstreams-hdfs-parquet.sql). This script demonstrates how to read parquet file(s) stored in HDFS.

1. Execute the [product-reviews-hdfs-csv.sql](product-reviews-hdfs-csv.sql). This script demonstrates how to read CSV file(s) stored in HDFS.
