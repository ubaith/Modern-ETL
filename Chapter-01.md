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
