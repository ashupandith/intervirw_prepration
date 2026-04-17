# Enterprise Data Platform Interview Question Bank

## Purpose
This is the master question bank for data architecture, Fabric, Databricks, Synapse, pipelines, modeling, governance, performance, and leadership interviews.

Use this file as the main revision checklist before data-platform-focused interview rounds.

---

## 1. Profile / Introduction / Role Fit
- Tell me about yourself from a data architecture perspective.
- What kind of enterprise data platforms have you designed?
- What is your experience across Fabric, Databricks, and Synapse?
- Which platform are you strongest in, and why?
- How do you position yourself differently from a Data Engineer or Solution Architect?
- Describe one end-to-end cloud data platform you designed on Azure.
- What is your role in architecture vs hands-on implementation?
- Have you defined data standards or reusable frameworks for teams?
- How do you approach a new enterprise data platform initiative from scratch?
- What type of stakeholders do you usually work with?

## 2. Enterprise Data Architecture
- How do you define an end-to-end data architecture for an enterprise platform?
- What are the major layers in a modern cloud data platform?
- How do you decide between Data Lake, Lakehouse, and Data Warehouse?
- What is your approach to building a scalable and modular data platform?
- How do you separate ingestion, transformation, serving, governance, and consumption layers?
- How do you design for multi-domain or multi-business-unit data architecture?
- How do you ensure the platform supports BI, analytics, and AI/ML together?
- What architectural principles do you follow while designing cloud data systems?
- How do you avoid creating another data silo in the cloud?
- What are the common mistakes organizations make when building modern data platforms?

## 3. Microsoft Fabric
- What is Microsoft Fabric, and how is it different from traditional Azure data services?
- Explain the key components of Fabric.
- What is OneLake, and why is it important?
- What is the role of Lakehouse in Fabric?
- When would you choose Fabric Data Factory over ADF or Synapse Pipelines?
- How do Fabric pipelines differ from Databricks workflows?
- How do notebooks work in Fabric?
- What are the advantages of Fabric for enterprise analytics?
- How do you manage governance and security in Fabric?
- How does Fabric integrate with Power BI?
- What are the limitations or risks of adopting Fabric in an enterprise?
- How would you design a Fabric-based architecture for a company starting fresh on Azure?
- How do you manage data movement and transformation in Fabric?
- What are shortcuts in Fabric, and where would you use them?
- How do you see Fabric coexisting with Databricks and Synapse in the same enterprise?

## 4. Azure Databricks
- Why would you choose Azure Databricks for an enterprise data platform?
- Explain the Databricks architecture at a high level.
- What is the difference between Spark SQL, PySpark, and SQL Warehouse?
- What is Delta Lake, and why is it important?
- What problems does Delta Lake solve compared to raw Parquet files?
- Explain ACID transactions in Delta Lake.
- What is the Delta transaction log?
- How do OPTIMIZE, VACUUM, and Z-ORDER help performance?
- How do you handle the small files problem in Databricks?
- How do you design bronze, silver, and gold layers?
- How do you implement schema evolution in Delta Lake?
- How do you handle late-arriving data in Databricks?
- How do you build incremental pipelines in Databricks?
- How do you optimize Spark jobs for performance?
- What are common reasons for slow Spark jobs?
- How do partitioning and file size affect performance?
- What are joins in Spark, and how do you tune large joins?
- What is broadcast join, and when would you use it?
- How do you design reusable ETL frameworks in Databricks?
- How do you schedule and orchestrate Databricks jobs?
- How do you manage secrets and credentials in Databricks?
- How do you implement CI/CD for Databricks notebooks and jobs?
- What is Unity Catalog, and why is it important?
- How do you design governance using Unity Catalog?
- How do you control access at catalog, schema, table, and column level?

## 5. Azure Synapse Analytics
- What are the core components of Azure Synapse Analytics?
- When would you choose Synapse over Databricks?
- How do Synapse Pipelines compare with ADF?
- How does Synapse SQL differ from Spark pools?
- What is the role of dedicated SQL pool vs serverless SQL pool?
- How do you architect data serving with Synapse?
- What kind of workloads are better suited for Synapse?
- What are the strengths and weaknesses of Synapse?
- How do you optimize Synapse SQL performance?
- How would you integrate Synapse with ADLS Gen2?
- How would you design a solution using both Synapse and Databricks?
- Where does Synapse still fit if an organization is moving toward Fabric?

## 6. ETL / ELT / Data Pipelines
- What is the difference between ETL and ELT?
- When would you prefer ETL vs ELT?
- How do you architect scalable data pipelines on Azure?
- What is your approach to batch ingestion design?
- How do you design metadata-driven pipelines?
- What is a reusable ingestion framework?
- How do you handle schema drift in pipelines?
- How do you design parameterized pipelines for multiple source systems?
- How do you implement incremental loading?
- How do you design CDC-based pipelines?
- How do you ensure idempotency in data pipelines?
- How do you handle pipeline retries and failure recovery?
- What logging and audit mechanisms do you implement in data pipelines?
- How do you support data quality validation in ETL and ELT flows?
- How do you decide whether transformation should happen in pipeline orchestration vs Spark processing?
- What are the pros and cons of orchestrating through ADF, Synapse Pipelines, Databricks Workflows, or Airflow?
- How do you manage dependencies between multiple pipelines?
- How do you design for reusability across projects?

## 7. Data Modeling / Storage Strategy
- Explain the difference between Data Lake, Lakehouse, and Data Warehouse.
- When would you use a Lakehouse instead of a Warehouse?
- What are the trade-offs of star schema vs snowflake schema?
- What is dimensional modeling?
- What are facts and dimensions?
- How do you handle slowly changing dimensions?
- Explain SCD Type 1 vs Type 2.
- How do you design data models for reporting and BI?
- How do you decide between normalized and denormalized models?
- How do you design storage for structured, semi-structured, and unstructured data?
- How do you organize zones in ADLS Gen2?
- How do you define retention, archival, and purge strategy?
- How do you design partition strategy in a data lake?
- How do you avoid excessive duplication across lakehouse and warehouse layers?
- How do you model data for both operational analytics and executive reporting?

## 8. Batch and Real-Time Architectures
- What is the difference between batch and streaming architectures?
- When should near-real-time processing be used instead of batch?
- How would you design a real-time ingestion architecture on Azure?
- What is your experience with Kafka or Event Hubs?
- How do you process streaming data in Databricks or Synapse?
- What is Structured Streaming?
- How do you handle late events and out-of-order events?
- How do you design real-time analytics with low latency?
- How do you maintain consistency between batch and streaming outputs?
- How do you decide whether the business really needs streaming?

## 9. AI / ML-Ready Data Platforms
- What does an AI and ML-ready data platform mean to you?
- How do you design data architecture to support AI and ML use cases?
- What kind of datasets are needed for feature engineering?
- How do you ensure data quality for ML pipelines?
- How do you manage historical training datasets?
- How do you support model reproducibility from a data architecture perspective?
- How do you design feature-store-like patterns on Azure?
- How do you support both batch scoring and real-time scoring?
- What data platform considerations are required for GenAI or advanced analytics use cases?
- How do governance and lineage become more important in AI and ML data platforms?

## 10. Governance, Security, Compliance
- How do you design data governance in a cloud data platform?
- What is your experience with Purview?
- How do you implement data lineage and data cataloging?
- How do you classify sensitive data?
- How do you design role-based access control for data platforms?
- How do you handle row-level and column-level security?
- How do you secure ADLS Gen2?
- How do you secure Databricks access to storage?
- How do you handle secrets and credentials securely?
- How do you meet compliance requirements like PII protection and auditability?
- What is your approach to encryption at rest and in transit?
- How do private endpoints and managed identities fit into data platform security?
- How do you define access patterns for analysts, engineers, data scientists, and business users?
- How do you balance governance with developer productivity?
- How do you prevent uncontrolled data copies across tools?

## 11. Performance, Scalability, Cost Optimization
- How do you optimize large-scale data platforms for performance?
- What are the common cost drivers in Databricks, Synapse, and Fabric?
- How do you reduce cost without impacting business SLAs?
- How do you choose between serverless and dedicated compute?
- How do you tune Spark jobs?
- How do you size clusters and workloads?
- How do you handle concurrency issues?
- How do you optimize storage and compute separation?
- How do you optimize query performance in lakehouse and warehouse architectures?
- How do you monitor pipeline duration and bottlenecks?
- How do you define performance benchmarking for a new platform?
- What are the trade-offs between performance and cost?
- How do you architect for scale as data volume grows 10x?

## 12. DevOps / CI-CD / IaC / Observability
- How do you implement CI/CD for a cloud data platform?
- What should be version-controlled in data projects?
- How do you handle notebook deployment in Databricks?
- What branching strategy do you recommend for data platform teams?
- What is your experience with Azure DevOps?
- How do you automate deployments using Terraform, Bicep, or ARM?
- What infrastructure components would you provision through infrastructure as code?
- How do you manage environment-specific configuration?
- How do you promote data pipelines across dev, test, and prod?
- How do you ensure safe release and rollback?
- How do you implement observability for data pipelines?
- What metrics and alerts should exist in a production data platform?
- How do you monitor data freshness, failure rate, and SLA breaches?
- How do you audit data pipeline executions end to end?

## 13. Tool Comparison / Decision Questions
- When would you choose Fabric vs Databricks?
- When would you choose Databricks vs Synapse?
- When would you choose Fabric vs Synapse?
- Can Fabric replace Synapse completely?
- Can Databricks replace traditional ETL tools?
- When should Power BI connect directly to Lakehouse vs Warehouse?
- When would you recommend dbt in an Azure data platform?
- What is the role of Airflow if Azure-native orchestration tools already exist?
- When do you use Data Factory vs notebooks vs SQL transformations?
- How do you decide the right combination of tools instead of using everything?

## 14. Scenario-Based / Design / Whiteboard Questions
- Design an enterprise data platform on Azure for a retail organization with ERP, CRM, and e-commerce sources.
- A client wants a Lakehouse platform supporting BI, self-service analytics, and ML. How would you design it?
- Design a modern data platform using Fabric, Databricks, and Synapse together.
- A company wants to migrate from on-prem ETL and SQL warehouse to Azure. What migration strategy would you follow?
- Design a platform for ingesting batch plus real-time data from multiple geographies.
- How would you design a governed self-service analytics platform?
- How would you architect a secure data platform for PII-heavy workloads?
- Design a feature-engineering data layer for ML teams.
- Design a medallion architecture with governance and cost optimization.
- A client wants near-real-time dashboards from operational systems. How would you design it?
- Your data volume will increase from 5 TB to 100 TB in 18 months. How will your architecture evolve?
- Business wants Fabric, engineering wants Databricks, and existing reporting uses Synapse. What architecture do you propose?
- If data pipelines are failing intermittently and business users are losing trust, how would you redesign the platform?
- How would you design DR, backup, and resilience for an Azure data platform?
- How would you build a metadata-driven reusable framework for multiple ingestion patterns?

## 15. Leadership / Ownership / Team Guidance
- How do you lead architecture decisions across multiple teams?
- How do you define architectural standards for engineering teams?
- How do you handle disagreements between engineering and business stakeholders?
- How do you mentor data engineers and technical leads?
- How do you ensure design quality in a fast-paced delivery model?
- How do you review a design before approving it?
- How do you manage technical debt in data platforms?
- How do you handle a situation where the team wants a quick fix but architecture requires a more scalable approach?
- How do you bring governance without slowing delivery?
- How do you handle estimation and solutioning at architecture level?

## 16. Behavioral Questions
- Tell me about a time when you designed a platform under tight timelines.
- Tell me about a time you improved performance or reduced cost significantly.
- Tell me about a time you handled a failed data migration or unstable pipeline.
- Tell me about a time when stakeholders had conflicting expectations.
- Tell me about a time you introduced a new architecture standard.
- Tell me about a time you influenced teams without direct authority.
- Tell me about a time you mentored junior engineers into stronger delivery.
- Describe a situation where your architecture recommendation was initially rejected.
- Tell me about a production incident in a data system and how you resolved it.
- Tell me about a time you had to balance ideal architecture with business urgency.

---

## Highest-Probability Questions to Practice First
1. Design an end-to-end enterprise data platform on Azure.
2. Fabric vs Databricks vs Synapse — when to use which.
3. Lakehouse vs Data Warehouse vs Data Lake.
4. How do you design scalable ETL and ELT frameworks?
5. How do you build AI and ML-ready data platforms?
6. How do you implement governance, security, and access control?
7. How do you optimize Databricks performance and cost?
8. How do you design bronze, silver, and gold architecture?
9. How do you handle real-time plus batch together?
10. How do you implement CI and CD plus infrastructure as code for data platforms?
11. How do you use Purview, lineage, and catalog in enterprise data architecture?
12. Tell me about one enterprise-scale data platform you architected.

---

## Tough Follow-Up Questions They May Ask
- Why not use only Fabric for everything?
- If Databricks is powerful, why keep Synapse?
- How do you prevent platform sprawl in Azure data programs?
- How do you justify the cost of multiple tools to leadership?
- How do you govern self-service analytics without creating chaos?
- How do you ensure one version of truth across lakehouse and warehouse?
- How do you design for both speed and governance?
- What is your strategy for multi-environment, multi-team platform management?
- Where would you place data quality checks?
- What is your approach to lineage, audit, and compliance from day one?

---

## Smart Questions to Ask the Interviewer
- Is the organization more invested in Fabric, Databricks, or Synapse as the long-term strategic platform?
- Is this role more architecture-heavy, or does it also involve hands-on design and delivery?
- Are the current data platforms centralized or domain-driven?
- What are the major challenges today: governance, performance, migration, or platform standardization?
- How mature is the organization in AI and ML data readiness?
- Does this role define reusable standards across teams?
- What would success look like in the first six months?

---

## Best Preparation Order for This Role
1. Architecture fundamentals: lakehouse, warehouse, data lake, medallion, dimensional modeling.
2. Platform comparison: Fabric vs Databricks vs Synapse.
3. Pipeline design: ETL, ELT, orchestration, CDC, incremental loads, metadata-driven frameworks.
4. Databricks depth: Delta Lake, Spark tuning, optimization, governance.
5. Fabric depth: OneLake, Lakehouse, pipelines, notebooks, Power BI integration.
6. Governance and security: Purview, RBAC, private endpoints, managed identity, data privacy.
7. Scenario design: practice at least 2 to 3 end-to-end architectures.
8. Leadership stories: cost optimization, mentoring, architecture decisions, stakeholder handling.
