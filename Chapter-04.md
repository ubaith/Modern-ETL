# Chapter 04: Pipeline Issues and Troubleshooting
## Maintainability
1. Monitoring and Benchmarking
   - required for minimizing pipeline issues and expediting troubleshooting efforts.
   - make it easier to improve the maintainability and lower the costs associated with broken data
   - Metrics
     * Freshness: timeliness and relevance of data in a system
       - The length between the most recent timestamp and the current timestamp
       - The lag between source data and target dataset
       - The refresh rate
       - Latency
     * Volume: The amount of data that needs to be processed, stored, and managed within a system
       - The size of a data lake
       - The number of rows in a database
       - The volume of daily transactions in a system
     * Quality: data accuracy, consistancy, reliability, timeliness, completeness, security, documentation, and monitoring
       - Uniqueness (No duplicates)
       - Completeness (No unexpected null values)
       - Validity (Proper format)
   - Methods
      * Logging and monitoring
      * Lineage
      * Anomaly detection
      * Data diffs
        - report on the data changes presented by changes in code
          * row and column changes
          * primary key counts
        - tools
          * Datafold
          * SQLMesh
      * Assertions
        - constraints put on data outputs to validate source
 2. Error Handling
    - approaches
      * Conditional logic
      * Retry mechanisms
      * Pipeline decomposition
      * Graceful degradation and error isolation
        - Error isolation is systems should be designed to fail in a contained manner
        - Graceful degradation is the ability to maintain limited functionality even when a part of the system fails.
      * Alerting
  3. Recovery
     - methods and concepts
       * Staging
       * Backfilling
  4. Improving Workflows
     - Relationships
       * SLAs
       * Data contracts
         - a type of assertion that check for metadata before executing part or all of an ETL pipeline
       * APIs
         - a method of transmitting an expected set of data
         - more granular access control, scalability benefits, and versioning
        * Compassion and empathy
     - Incentives
       * Number of incidents (N)
       * Time to detection (TTD)
       * Time to resolution (TTR)
       * Data downtime (N × [TTD + TTR])
       * Cost
  5. Improve Outcomes
     - Documentation
     - Postmortems
     - Unit tests
     - CI/CD
     - Simplification and abstraction
     - Data systems as code
