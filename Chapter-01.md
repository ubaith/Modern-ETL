# Chapter 01: Data Ingestion

## Source checklist
1. Who will we collaborate with?
2. How will the data be used?
3. Are there multiple sources?
4. What’s the format?
5. What’s the frequency?
6. What’s the volume?
7. What processing is required?
8. How will the data be stored?

## Destination checklist
1. Who will we collaborate with?
2. How will the data be used?
3. Are there multiple destinations?
4. What’s the format?
5. What’s the frequency?
6. What’s the volume?
7. What processing is required?
8. How will the data be stored?

## Ingestion Considerations
1. Frequency
   1. Batch
   2. Micro-batch
   3. Streaming
         - methods
           1. Windowing
           2. Fixed windows
           3. Sliding windows
           4. Sessions
           5. Time-agnostic
         - Message services
           1. Apache Kafka
           2. Redpanda
           3. Pub/Sub
           4. Kinesis
         - Processing Engines
           1. Apache Flink
           2. Apache Spark Structured Streaming
           3. Apache Kafka Streams
         - Simplifying stream processing
           1. Managed platforms
           2. Confluent Kafka
           3. Bytewax
        
2. Payload
   1. Volume
      - factors to consider
         1. Cost
         2. Latency
         3. Throughput/scalability
         4. Retention
   2. Structure and shape
         1. Unstructured
         2. Semi-structured
            - XML
            - JSON
         3. Structured
   3. Format
   4. Variety

## Choosing a Solution
1. Declarative Solutions
   - Types
     1. Legacy
        1. Talend
        2. WhereScape
        3. Pentaho
     2. Modern
        1. Fivetran
        2. Stitch
        3. Airbyte
     3. Native
        1. Databricks
   - Cost to build/maintain
     * Dedicated support will be available from the vendors
   - Extensibility
     * Extensibility is crucial. A lack of extensibility can lead to the need for multiple solutions, increasing costs and complexity.
   - Cost to switch
     * vendor lock-in and switching to a different tool can be costly
2. Imperative Solutions
   - Types
     1. Singer Tap
     2. Lambda Function
     3. Apache Beam templates
     4. Job Orchestration
        * Apache Airflow
   - Extensibility
     * tailored to the needs of the business but need large data engineering team
   - Cost to build/maintain
     * Time consuming and amplyfing complexity
   - Cost to switch
     * potentially offering a smoother switch
3. Hybrid Solutions
   - Mix of following
     1. Fivetran and in-house solutions for unique sources
     2. Airbyte/Meltano and custom components for unsupported data sources
     3. dlt
