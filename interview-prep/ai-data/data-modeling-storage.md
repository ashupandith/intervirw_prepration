# Data Modeling and Storage Strategy Interview Notes

## Purpose
This file prepares you for architect-level questions on lake vs lakehouse vs warehouse, dimensional modeling, SCDs, schema strategy, partitioning, and data serving design.

---

## Data Lake vs Lakehouse vs Data Warehouse
### Data Lake
Best for raw, flexible, multi-format storage at scale.

### Lakehouse
Best when you want data lake flexibility with stronger structure, reliability, and analytics readiness.

### Data Warehouse
Best for curated, high-trust, structured analytical serving and BI consumption.

**Interview answer:**
I do not treat these as competing buzzwords. I treat them as serving different needs in the data lifecycle. In many enterprise architectures, they coexist as part of the same platform strategy.

---

## Dimensional Modeling
Dimensional modeling organizes data into facts and dimensions to support reporting performance, usability, and business clarity.

### Facts
Quantitative events or measures.

### Dimensions
Descriptive business context such as customer, product, geography, or time.

---

## Star vs Snowflake
### Star schema
- simpler for BI use and query performance
- easier for business users to understand

### Snowflake schema
- more normalized and can reduce redundancy
- may add complexity for reporting users

---

## Slowly Changing Dimensions
### Type 1
Overwrite old values when history is not needed.

### Type 2
Preserve historical versions when business history matters.

---

## Storage Strategy Principles
- organize raw, refined, and curated zones clearly
- partition based on access patterns, not habit
- avoid unnecessary data duplication
- define retention, archival, and purge rules early
- design for both analytical access and governance needs

---

## Common Interview Questions
- When would you use a lakehouse instead of a warehouse?
- What are the trade-offs of star schema vs snowflake?
- How do you handle slowly changing dimensions?
- How do you organize zones in ADLS Gen2?
- How do you design storage for structured and semi-structured data?

---

## Strong Sample Answer
### Q: How do you decide between lakehouse and warehouse?
**Tags:** [Data] [Modeling] [Architecture]

**Answer:**
I decide based on the consumption pattern, data variety, transformation complexity, governance needs, and whether the platform must support BI, advanced analytics, and ML together. If the need is broader engineering flexibility with analytics readiness, a lakehouse often fits well. If the priority is highly curated and predictable BI serving, a warehouse may be the better primary layer.
