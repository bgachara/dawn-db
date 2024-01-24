# Composable Database

- This is Rust implementation of a composable database following the paper by the same name.

## Main parts

- *Scheduler:* 
- Responsible for sending query plan fragments to execute nodes and updating internal task state.

- *Execution engine:* 
- Executes physical plan operators to retrieve data, process tuples and generate output. Single node only.

- *Catalog service:* 
- Internal database of data files and table schemas.

- *I/O service and distributed cache:* 
- Provides an access layer to retrieve and cache blocks from data files.

- *Query Optimizer*
- Generate an efficient physical plan for a SQL statement using rule-based optimizations and cost-based search, take inspiration from `apache arrow datafusion`.

## Project proposal

- Write a plan on how to implement their component and present high-level topic.
- Each proposal must discuss
  - Architecture and implementation overview of the project.
  - How will you test whether implementation is correct.
  - What workloads you will use for your project.
- Include the API specification of the component
  - supported commands/operations
  - input/output encodings.
  - status codes/ Error handling.
- Look into the open source Apache Iceberg API to ensure implementations are interchangeable.

## Status updates

- Current development status
- Whether you plan has changed and why.
- Anything that surprised you during coding.
- Testing code coverage.

- Design document that describes current state of your project's implementation
  - Architectural design.
  - Design rationale.
  - Testing plan.
  - Trade-offs and potential problems.
  - Future work.
