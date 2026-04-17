# Data Governance, Security, and Compliance Interview Notes

## Purpose
This file covers governance, Purview, lineage, RBAC, sensitive data controls, private connectivity, compliance, and balancing control with delivery speed.

---

## Governance Principles
- ownership must be clear
- data should be discoverable and classified
- access should be role-based and least privilege
- lineage and audit must exist from day one
- governance should enable reuse, not block delivery

---

## Security Controls to Mention
- managed identities where possible
- Key Vault for secrets
- private endpoints for sensitive services
- encryption at rest and in transit
- RBAC plus fine-grained controls where supported
- row-level and column-level security for sensitive consumption scenarios

---

## Purview Interview Positioning
I position Purview as the governance layer that helps with discovery, classification, lineage, and policy alignment across a growing data estate. It becomes especially valuable when multiple domains and tools are involved and the organization wants trust and visibility rather than unmanaged data sprawl.

---

## Common Interview Questions
- How do you design governance in a cloud data platform?
- What is your experience with Purview?
- How do you implement lineage and cataloging?
- How do you secure ADLS Gen2 and Databricks access to storage?
- How do you balance governance with developer productivity?
- How do you prevent uncontrolled data copies across tools?

---

## Strong Sample Answer
### Q: How do you implement governance and security in a modern Azure data platform?
**Tags:** [Data] [Security] [Governance] [ArchitectRole]

**Answer:**
I design governance as part of the platform foundation rather than a later compliance overlay. That means clear ownership, classification of sensitive data, role-based access, auditability, lineage, and secure connectivity patterns such as managed identities and private endpoints.

At the same time, I try to avoid governance models that slow teams down unnecessarily. The best approach is to provide secure defaults, reusable standards, and automated controls so teams can move quickly without bypassing policy.
