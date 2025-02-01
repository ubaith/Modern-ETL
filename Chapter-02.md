# Chapter 02: Data Transformation
## How Do We Transform Data?
1. Environments
   - Data warehouses
   - Data lakes
   - Data lakehouses
2. Data staging
   - Medallion architecture in Data Lake or Lakehouse
     * Bronze : raw and unfiltered
     * Silver : filtered, cleaned, and adjusted
     * Gold : generally stakeholder-ready and sometimes aggregated
   - Transform data in data warehouse
     * Staging
     * Curated
     * Marts
3. Languages
   - Python
     * choose a suitable library: Pandas or Polars or DuckDB
     * selecting a framework for orchestrating and executing the transformation
   - SQL
   - Rust
4. Frameworks
   - Hadoop
   - Spark
   - Database or SQL Engines
     * BigQuery
     * RedShift
     * Snowflake

## Building a Transformation Solution
1. Data Transformation Patterns
   - Enrichment
     * enhancing existing data with additional sources
     * involve joining on internal structures or fetching additional data from external source
   - Joining
     * 
