# System Design Interview Playbook

## Objective
This file is your primary framework for answering architecture and system design questions in a senior architect interview.

The goal is to sound structured, calm, and decisive.

---

## Best Opening Line in a System Design Round
A strong opening is:

> I will begin by clarifying the business goal, scale assumptions, and non-functional requirements, then I will propose an architecture and explain the trade-offs.

This immediately signals seniority.

---

## Standard Answer Structure
Use this flow every time:

## 1. Requirements
- business objective
- users and personas
- main functional flows
- expected scale and availability needs

## 2. Assumptions
- unclear areas you are explicitly assuming
- constraints around time, budget, compliance, or legacy systems

## 3. High-Level Architecture
- client channels
- API layer
- application/services layer
- data layer
- integration and messaging
- external systems

## 4. Scalability
- stateless services
- autoscaling
- caching
- async processing
- partitioning or sharding if needed

## 5. Security
- identity and access control
- encryption in transit and at rest
- secrets management
- network isolation and edge protection

## 6. Observability
- logs, metrics, traces
- alerting strategy
- health and dependency monitoring

## 7. Trade-Offs
- why this design instead of plausible alternatives
- what is intentionally postponed
- how cost and complexity are being controlled

## 8. Risks
- hot spots, bottlenecks, third-party dependency risk, data quality risk

## 9. Final Recommendation
- summarize the architecture and why it best fits the scenario

---

## Interview-Ready System Design Language
Use phrases like:
- "I would optimize first for clarity of domain boundaries and operational simplicity."
- "I would avoid over-engineering unless the scale or organizational model truly demands it."
- "Security and observability would be built in from the start rather than treated as follow-up work."
- "I would validate the assumptions that have the biggest impact on architecture choice."

---

## Common System Design Prompts to Practice
- design a scalable e-commerce platform
- design a document management platform for an enterprise
- design a booking or order processing platform
- design a multi-tenant SaaS solution
- design a GenAI-powered internal knowledge assistant
- design an event-driven integration platform on Azure

---

## Sample Mini Answer: Enterprise Order Platform
**Requirements:** support online order capture, payment, status tracking, and high seasonal peaks.

**Architecture:** API gateway, order service, payment integration, inventory service, event bus, operational database, cache, and monitoring stack.

**Scalability:** stateless services, async order events, caching for read-heavy operations, queue buffering for downstream dependencies.

**Security:** identity, secure API access, encryption, secrets management, and fraud-related controls.

**Observability:** end-to-end tracing, business metrics, alerting on order failures and latency.

**Trade-offs:** use synchronous calls only where immediate consistency is essential, and event-driven flow where decoupling improves resilience.

---

## Mistakes to Avoid
- diving into services before clarifying requirements
- giving only infrastructure names without architecture flow
- ignoring operations and monitoring
- forgetting security and data strategy
- sounding like a developer solving only one component

---

## Revision Notes
- structure matters as much as content
- slow down and think visibly
- show trade-offs, not just components
