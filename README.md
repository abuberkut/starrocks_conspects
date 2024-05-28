# Starrocks
- analytical dwh
- mpp architecture
- real-time, batch data ingestion
- ad-hoc queries

## Catalogs, databases, and tables

Starrocks consists of:
- Internal Catalog (Data stored in Starrocks)
  - DB1{Tbl, View, MView,...}
  - DB2{Tbl, View, MView,...}
  - ...
- External Catalog 1 (Data stored in external data sources)
  - DB1{Tbl1, ..., TblN},
  - DB2{Tbl1, ..., TblN},
  - ...
- External Catalog 2 (Data stored in external data sources)
  - DB1{Tbl1, ..., TblN},
  - DB2{Tbl1, ..., TblN},
  - ...
 
### Catalogs 
Each cluster has only one Internal catalog **default_catalog** and manages the data loaded into the cluster and the materialized views
StarRocks can well serve as a data warehouse 
External catalog - you can use StarRocks as a query engine to directly query data in the lake without loading the data into StarRocks
### > lake = external data?

### Databases

### Tables
Internal tables are maintained in internal catalogs, in databases under the internal catalog. Internal tables types - `Primary Key tables`, `Duplicate Key tables`, `Aggregate tables`, and `Unique Key tables`

External tables
