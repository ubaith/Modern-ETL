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
