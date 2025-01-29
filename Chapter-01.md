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
   a. Batch
   b. Micro-batch
   c. Streaming
      - methods
           i. Windowing
           ii. Fixed windows
           iii. Sliding windows
           iv. Sessions
           v. Time-agnostic
      - Message services
           i. Apache Kafka
           ii. Redpanda
           iii. Pub/Sub
           iv. Kinesis
      - Processing Engines
           i. Apache Flink
           ii. Apache Spark Structured Streaming
           iii. Apache Kafka Streams
      - Simplifying stream processing
           i. Managed platforms
           ii. Confluent Kafka
           iii. Bytewax
        
2. Payload
4. format
5. processing
