# Microsoft Fabric Interview Notes

## Purpose
This file is for architect-level interview preparation on Microsoft Fabric, OneLake, lakehouse-based analytics, governance, and how Fabric fits into an enterprise Azure data strategy.

---

## What is Fabric?
Microsoft Fabric is a unified SaaS analytics platform that brings together data movement, data engineering, lakehouse, warehouse, real-time analytics, and Power BI in one integrated experience.

### Why it matters in interviews
Interviewers are not only checking whether you know the product. They want to know whether you can explain:
- where Fabric fits well
- where it does not fully replace other tools
- how it helps simplify platform sprawl
- what trade-offs exist for enterprise adoption

---

## Key Components to Revise
- OneLake
- Lakehouse
- Warehouse
- Data Factory in Fabric
- notebooks and Spark workloads
- Real-Time Intelligence
- Power BI integration
- security and governance model

---

## OneLake and Why It Matters
OneLake is Fabric’s unified logical data lake. It reduces fragmentation and makes shared enterprise data easier to discover, reuse, and govern.

**Interview angle:**
I position OneLake as a simplification layer for enterprise analytics, especially where teams want less platform sprawl and tighter integration across ingestion, transformation, and reporting.

---

## When to Choose Fabric
Use Fabric when:
- the organization wants an integrated analytics platform
- Power BI is already strategic
- the business wants faster time to value with less tool fragmentation
- self-service analytics and governed sharing are key goals

Do not position Fabric as the answer to every data problem. It may not fully replace more specialized engineering-heavy platforms in every scenario.

---

## Fabric vs Databricks vs Synapse
### Fabric
- best for unified analytics experience
- strong Power BI alignment
- simpler integrated operating model

### Databricks
- stronger for advanced data engineering, Spark-heavy workloads, and deeper platform flexibility
- often preferred for complex large-scale transformation and ML engineering

### Synapse
- still relevant where existing SQL-serving or integrated analytical patterns already exist
- useful in some transition states and mixed estates

**Architect answer:**
I choose based on workload complexity, team maturity, BI strategy, governance model, and whether the business needs simplification or deep engineering flexibility.

---

## Enterprise Risks and Trade-Offs
- platform immaturity in some scenarios compared with longer-established patterns
- need for governance discipline even in a simplified toolset
- risk of assuming one platform should absorb every workload
- cost and licensing must still be justified by business usage patterns

---

## Common Interview Questions
- What is Microsoft Fabric, and how is it different from traditional Azure data services?
- What is OneLake, and why is it important?
- When would you choose Fabric over Databricks or Synapse?
- How do Fabric pipelines compare with ADF or Databricks workflows?
- What are the enterprise benefits and limitations of Fabric adoption?
- How would you design a Fabric-first architecture for a new organization on Azure?

---

## Strong Sample Answer
### Q: How do you see Fabric fitting into an enterprise data platform?
**Tags:** [Fabric] [Data] [Architecture] [ArchitectRole]

**Answer:**
I see Fabric as a strong option when the organization wants a more unified analytics experience with tighter integration across ingestion, lakehouse, warehousing, and Power BI. It can reduce platform fragmentation and accelerate delivery for analytics-focused teams.

That said, I would still evaluate where specialized workloads may be better served by Databricks or existing Synapse patterns. My recommendation would depend on engineering complexity, governance expectations, the reporting operating model, and long-term platform standardization goals.

---

## Revision Notes
- talk about Fabric as simplification plus integration
- mention OneLake and Power BI synergy
- acknowledge that coexistence with Databricks or Synapse is often realistic in large enterprises
