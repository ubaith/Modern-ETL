# Chapter 03: Data Orchestration
- process of dependency management
- data orchestrator manages
  * scheduling
  * triggering
  * monitoring
  * resource allocation
- Orchestrators can trigger on
  * Events
  * Webhooks
  * schedules
  * intra-workflow dependencies
- Why Orchestrate
  * Workflow management: ensuring tasks are executed in the right order by managing dependencies
  * Automation: automate routine,repetitive, and complex tasks
  * Error handling and recovery: retry a failed task, notify or trigger other tasks to fix the issue.
  * Monitoring and alerting
  * Resource optimization
  * Observability and debugging
  * Compliance and auditing
- The DAG (directed acyclic graph)
  *  describe a “tree” of data execution where “tasks” are represented as nodes and “dependencies” are edges
  *  Directed: indicating the presence of dependencies within the graph
  *  Acyclic: There are no cycles in our tree
  *  bring order, control, and repeatability to data workflows
## Data Orchestration Tools
- Choosing an Orchestrator
  1. Characteristics
     - Scalability: matter of handling complex logic and dependencies
     - Code and configuration reusability: Anything that is done more than once should be converted to a function or class
     - Connections: ensuring a wide library of native connections
     - Support
     - Observability: necessary visibility into the status of your data pipelines
  2. Orchestrator options
     - Build a solution
     - Buy an off-the-shelf tool
     - Self-host an open source tool
       * Apache Airflow
        * Prefect
        * Dagster
        * Mage (pre-v1)
        * Keboola (pre-v1)
        * Keboola (pre-v1)
     - Use a tool included with your cloud provider or data platform
       * ADF
       * Databricks Workflows
      - Options available
        * Apache Airflow
        * Prefect
        * Dagster
        * Mage (pre-v1)
        * Keboola (pre-v1)
        * Keboola (pre-v1)
 - Orchestrating SQL
   * data transformation has its own concept of orchestration
   * data is written to a source system, then transformed sequentially with complex SQL queries and manipulations
   * Tools: dbt, Delta Live Tables, Dataform, or SQLMesh
      - evaluate dependencies and conditions,then optimize and execute commands against a database to produce desired result
   * platform-specific data orchestrator gives visibility (Lineage), both between and within data workflows
## Design Patterns and Best Practices
- Backfills
  * anything done once should be repeatable
  * Ex: Airflow DAGs allow set a past start_date to trigger a run that recreates historical data
- Idempotence
  * ensuring doing something multiple times yields consistent results
- Event-driven orchestration
  * allows for reactivity to changes in data or system states
  * Ex: Transformation starting after the ingestion finishes
- Conditional logic
  * allows further automate the ETL process
  * account for errors, failures, or malformed data
- Concurrency
  * Orchestrators are obviously capable of running concurrent pipelines
- Fast feedback loops
  * tool that allows to fail fast and identify errors quickly
- Retry and fallback logic
  * handling failures well ensures data integrity and system reliability
  * Conditional logic can be paired with retry/fallback logic to create scenarios that gracefully handle errors
- Parameterized execution
  * allows for further malleability in orchestration and allows reuse pipelines for multiple purposes
- Lineage
  * the path traveled by data through its lifecycle
  * column-level lineage: a column-level view of data’s journey, from ingestion to analysis
- Pipeline decomposition
  *  ensuring tidy, readable pipelines is to break them down into smaller
  *  build autonomous DAGs that can be run in parallel to mitigate dependencies and critical failures
  *  Modular design will also make it easier to build and debug workflows
