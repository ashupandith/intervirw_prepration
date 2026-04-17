# ETL / ELT / Data Pipelines Interview Notes

## Purpose
This file covers architect-level answers for ingestion, transformation, orchestration, metadata-driven frameworks, CDC, idempotency, and pipeline reliability.

---

## ETL vs ELT
### ETL
Transform before loading into the analytical store.

### ELT
Load first, then transform inside the target platform.

**Interview answer:**
I choose ETL or ELT based on source constraints, transformation complexity, compute economics, data quality needs, and the capabilities of the target platform. In modern cloud platforms, ELT is often preferred because scalable cloud compute can perform transformations efficiently after landing the data.

---

## What Good Pipeline Architecture Looks Like
- clear ingestion zone separation
- metadata-driven and parameterized design
- reusable framework for common source patterns
- incremental and CDC-based loading where practical
- idempotent processing and safe retries
- audit logging, lineage, and data quality checkpoints

---

## Metadata-Driven Framework
A metadata-driven framework stores source configuration, schema expectations, scheduling rules, load types, and target mappings externally so the same pipeline pattern can be reused across many sources.

**Why this matters:**
It improves scale, consistency, and maintainability across enterprise data programs.

---

## CDC and Incremental Loading
Use CDC or watermark-based incremental loads when:
- source systems are large
- full reloads are inefficient
- business needs fresher data with lower cost

Always pair incremental logic with reconciliation and audit checks.

---

## Orchestration Choices
### ADF or Fabric pipelines
- strong for orchestration, movement, scheduling, dependency control

### Databricks Workflows
- stronger when the transformation logic is notebook or job heavy

### Airflow
- useful when there is broader cross-platform orchestration need and the team already has maturity around it

---

## Common Interview Questions
- What is the difference between ETL and ELT?
- How do you design scalable data pipelines on Azure?
- What is a reusable ingestion framework?
- How do you handle schema drift and pipeline recovery?
- How do you ensure idempotency in data flows?
- How do you decide whether logic belongs in orchestration or Spark transformation?

---

## Strong Sample Answer
### Q: How do you design scalable ETL or ELT frameworks?
**Tags:** [Data] [ETL] [ELT] [ArchitectRole]

**Answer:**
I design pipelines as reusable platform capabilities rather than one-off project scripts. That means standard ingestion patterns, metadata-driven configuration, incremental loading where possible, audit and data quality checkpoints, and consistent observability across every flow.

I also separate orchestration from heavy transformation logic so the platform stays maintainable. My goal is to make onboarding a new source repeatable, governed, and low-friction rather than rebuilding the same logic each time.
