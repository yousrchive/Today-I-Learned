## OLTP(Online Transaction Processing)

Database to be used for transaction
`No intermediate status`; Order should be done
All or None
INSERT, UPDATE action is frequently done.

`Not` mainly used for `analytics`.
Querying can be time-consuming.

## OLAP

to overcome limitation from shortage of analytics
provide tools for analyzing

DataWarehouse
Database, Web(Crawled) file, output of API

## `BIGQUERY`

Don't need to occupy server/computer for utilizing datawarehouse;
`Google` does manage its infrastructure

`Cloud-based`

related to `Firebase`, `Google Analyics4`

## Reason to Know How to Use BigQuery

> BigQuery Pricing

`Compute Pricing`

Price admitted per data processed

Rational querying does matter

`Storage Pricing`

## Google BigQuery

Google BigQuery is a serverless service or data warehouse that is `embedded with query engine`, having higher `scalability`(extensibility)

A paradigm called `MapReduce` is used in the service.

## ELT workflow

BigQuery allows users to extract and load raw data directly and then immediately transform that data using `BigQuery views`.

Interacting primarily with BigQuery through SQL, as it is a SQL engine, you can use various `business intelligence tools` such as Tableau, Looker, and `Google Data Studio` to create impactful analyses, visualizations, and reports with the data stored in BigQuery.

It supports the creation of `machine learning models and batch prediction tasks`.

BigQuery can store various types of data, including `geospatial data and hierarchical data`.

It supports both batch data collection and streaming data ingestion. You can stream data directly into BigQuery through the `REST API`.

As there is no need to build your own infrastructure, it reduces the hassle of ensuring `security`. Data in BigQuery is automatically encrypted both at rest and in transit.

## Settings

> Hierachy

`Project` > `Dataset`(including Tables that have the same intentions like Sales Dataset, Customer Datasets) > `Table`(Details)


Upload existing files to Google Cloud following below: 


A row is jumped and ignored; As the first row is just mentioning about what's heading to the following rows;
just for further explanation

Icon shape of 'Battle' table is different with others;
As the table is divided by `partitions`.

