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
- Data Transformation Patterns
  1. Enrichment
     * enhancing existing data with additional sources
     * involve joining on internal structures or fetching additional data from external source
  2. Joining
     * involves combining two or more datasets based on a common field
  3. Filtering
     * select only the necessary data points for analysis based on certain criteria
  4. Structuring
     * translating data into a required format or structure
  5. Conversion
     * changing the data type of a particular column or field
  6. Aggregation
     * summarizing and combining data
  7. Anonymization
     * masking or obfuscation of sensitive information within a dataset to protect privacy like hashing emails or otherwise removing PII
  8. Splitting
     * dividing a single complex data column into multiple columns
  9. Deduplication
     * removing redundant records to create a unique dataset
- Data Update Patterns
  1. Overwrite
  2. Insert
  3. Upsert
  4. Delete
- Best Practices
  1. Staging
     * protect against data loss
     * ensure a low time to recovery
   2. Idempotency
      * ensures consistency and reliability
      * doing something multiple times yields consistent results or reproducibility
      * crucial for handling failures and ensuring data consistency in distributed systems
   3. Normalization and denormalization
      * normalized data is unique and sometimes has a primary key
      * Denormalization involves duplicating records and information to make a system more performant
   4. Incrementality
      * defines whether pipeline is a simple INSERT OVERWRITE or a more complex UPSERT
## Real-Time Data Transformation
- True streaming transformations can be done using Beam, Flink, Kafka
- micro-batch transformations can be effective streaming transformations when latency is low enough using Apache Spark with PySpark or Spark SQL
- Spark Structured Streaming is a popular streaming application with features
  * streaming aggregations
  * eventtime windows
  * stream-to-batch joins
- 
