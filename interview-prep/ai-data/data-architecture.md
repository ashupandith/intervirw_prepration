# Data Architecture Interview Notes

## Purpose
This file covers enterprise data architecture, domain ownership, governance, storage patterns, analytics enablement, and end-to-end Azure data platform design.

---

## What Interviewers Want to Hear
For senior data architecture roles, the expectation is not a tool list. The expectation is that you can:
- define the end-to-end platform shape
- separate ingestion, transformation, serving, and governance layers clearly
- support BI, self-service, and AI on the same governed foundation
- make pragmatic choices across Fabric, Databricks, Synapse, storage, and security

---

## Major Layers in a Modern Data Platform
### 1. Source and ingestion layer
- ERP, CRM, line-of-business systems, SaaS platforms, files, APIs, and event streams
- batch, CDC, and streaming ingestion patterns

### 2. Raw landing layer
- immutable or minimally altered data
- auditability and replay support
- preserved source fidelity

### 3. Transformation and processing layer
- cleansing, standardization, conformance, enrichment
- batch and streaming transformations
- business rule application

### 4. Curated serving layer
- lakehouse or warehouse-ready datasets
- semantic models for reporting and analytics
- domain-oriented data products where relevant

### 5. Governance and security layer
- catalog, lineage, classification, RBAC, and auditability
- privacy and retention controls

### 6. Consumption layer
- BI, dashboards, advanced analytics, ML, GenAI, APIs, and self-service access

---

## Architecture Principles I Would State in Interviews
- separate storage from compute where it improves scale and flexibility
- design for reuse, not one-off pipelines
- keep raw data recoverable and traceable
- treat governance as a platform capability, not an afterthought
- prefer modular domain-aligned design over one giant central data mess
- balance self-service enablement with strong trust and control

---

## Strong Interview Answer
### Q: How do you define an end-to-end enterprise data architecture?
**Tags:** [Data] [Architecture] [ArchitectRole]

**Answer:**
I start by understanding the business use cases, data domains, latency expectations, compliance needs, and consumer types such as BI users, analysts, data scientists, and downstream applications. From there, I define a layered architecture with clear separation between ingestion, storage, transformation, serving, governance, and consumption.

I usually design the platform so that raw data is preserved, transformations are reusable, curated data products are governed, and access is aligned to business roles. I also make sure the platform supports more than reporting alone by enabling analytics and AI workloads on the same trusted foundation. My goal is to create a scalable, modular platform that reduces duplication and improves trust in data over time.

---

## How I Avoid Cloud Data Silos
- common storage and catalog strategy
- reusable ingestion and transformation patterns
- clear data ownership model
- semantic alignment across domains
- centralized governance with federated execution where needed

---

## Common Mistakes Organizations Make
- buying tools before defining architecture principles
- mixing raw, curated, and reporting data without discipline
- weak ownership and no data product mindset
- poor metadata, lineage, and trust controls
- over-centralizing everything or allowing uncontrolled sprawl

---

## Revision Notes
- speak in layers, governance, and consumption patterns
- emphasize platform thinking, not project-only thinking
- always connect architecture choices to trust, reuse, scale, and AI readiness
