# Azure Synapse Analytics Interview Notes

## Purpose
This file prepares you for architect-level questions on Synapse components, SQL-serving patterns, Spark, pipelines, and where Synapse fits alongside Fabric and Databricks.

---

## Core Components
- Synapse Pipelines
- dedicated SQL pool
- serverless SQL pool
- Spark pools
- workspace integration with ADLS Gen2

---

## When Synapse Fits Well
Use Synapse when:
- SQL-based analytics and enterprise reporting are central
- the organization already has Synapse investments
- there is a need for combined analytics workspace capabilities
- the team wants strong SQL-serving patterns in the Azure estate

---

## Dedicated vs Serverless SQL Pool
### Dedicated SQL pool
- provisioned performance
- useful for predictable analytical workloads
- stronger for curated warehouse-style serving

### Serverless SQL pool
- query-on-demand over data in the lake
- useful for lightweight exploration and cost-efficient ad hoc access
- not the right fit for every high-concurrency serving scenario

---

## Synapse vs Databricks
- Databricks is usually stronger for advanced engineering-heavy Spark workloads and flexible lakehouse processing
- Synapse is often attractive where integrated SQL analytics and Azure-native workspace patterns matter more

**Interview answer:**
I would not present them as mutually exclusive in every enterprise. Many organizations use Databricks for transformation and Synapse or equivalent SQL-serving patterns for curated analytics consumption.

---

## Synapse in a Fabric World
If an organization is moving toward Fabric, Synapse can still remain relevant during transition phases, especially where there are established workloads, SQL-serving dependencies, or migration sequencing constraints.

---

## Common Interview Questions
- What are the core components of Synapse?
- When would you choose Synapse over Databricks?
- How does Synapse SQL differ from Spark pools?
- How would you integrate Synapse with ADLS Gen2?
- Where does Synapse still fit if the organization is adopting Fabric?

---

## Strong Sample Answer
### Q: When would you choose Synapse in an enterprise architecture?
**Tags:** [Synapse] [Data] [Architecture]

**Answer:**
I would choose Synapse when the workload leans heavily toward SQL-based analytical serving, integrated Azure-native analytics patterns, and existing enterprise alignment with Synapse capabilities. It is especially useful when curated reporting and SQL consumption are central requirements.

If the requirement is more engineering-heavy, Spark-intensive, or ML-oriented, I would more strongly evaluate Databricks. In practice, the right answer is often coexistence rather than forced tool replacement.
