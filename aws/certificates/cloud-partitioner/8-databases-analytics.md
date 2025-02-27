# 8 Database

data on disk can have limits if data is structure, want index

## relational db
- use sql lang

## no sql db
- non-sql, non relational db
- allow flexible schema
- easy to evolve data model
- scalability and high perfomance
- kv, docs, graph, in-memory, search db, json

## OS Patching is handled by AWS, backup and restore and upgrade is as-well

## RDS
- postgre, mysql, maria, oracle, sql server, ibm db2, aurora (aws proprietary)
- auto provisioning, os patching
- point in time restore
- mutli AZ setup
- cannot SSH into instance

## aurora
- pay per second
- proxy fleet  

## RDS Deployment
- Read Replicas, data only written to the main DB
- Multi-AZ
    - failover in case of AZ outage
- Multi-region (read replicas)

## ElasticCache (Redis)
- caches are in memory databases with high performance, low latency

## Dynamo DB
- NoSQL, replica across 3 AZ, serverless database, low latency
- key value db
- primary key: partition key and sort key (type)
- products, schema defined per item

## DAX accelerator
- in memory cache for Dynamo DB

## Global table: read write to any AWS Region

## Redshift
- based on postgresql, not used for OLTP
- for OLAP, analytics, data warehousing
- load data once evry hr, not every sec
- sotored in column, not row based
- MPP Massively Parallel Query execution 

## Redshift Serveless, without managed data warehouse infra, realtime analytics, dashbording

## EMR: elastic MapReduce
- hadoop cluster (big data), analyze and process vast data
- support spark, hbase, presto
- support ML

## Athena
- analytics against S3 Object, sql lang to query
- support CSV, json, avro, parquet
- QuickSight (reporting & dashboards)
- severless SQL IN S3

## QuickSight
- dashboards, ml-powered BI
- RDS, Aurora, Athena, Redshift

## DocumentDB
- MongoDB NoSQL
- store JSON 
- Aurora is AWS of Postgre/MySQL

## Neptune
- Graph dataset, social network

## Timestream
- time series database

## Managed Blockchain
- join public blockchain network
- execute transaction without central authority

## Glue
- Manged ETL service
- prepare and transform data for analytics
- full serverless
- from s3, RDS, etc, extract and load to Redshift
- data catalog: catalog of dataset (schema central repo)

## DMS
- databased migration service