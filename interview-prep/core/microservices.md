# Microservices Interview Notes

## Purpose
This file captures architect-level thinking on microservices, service decomposition, communication, resilience, and governance.

---

## Core Concepts
- domain boundaries and bounded contexts
- synchronous vs asynchronous communication
- service autonomy and ownership
- eventual consistency and compensating actions
- observability across distributed systems

---

## Interview Angle
A strong answer should explain **when microservices are justified** and when a modular monolith is the better starting point.

---

## Starter Questions
- When would you choose microservices over a monolith?
- What are the biggest trade-offs of microservices?
- How do you handle distributed transactions?
- How do you avoid tight coupling between services?

---

## Sample Architect Answer
I do not treat microservices as a default target. I use them when there is clear value in independent scaling, deployment, team ownership, or domain isolation. If those drivers are weak, I prefer a simpler architecture first and evolve when justified.

---

## To Expand Later
- service boundary heuristics
- saga vs orchestration patterns
- event-driven microservices on Azure
- service mesh and when not to use it
- common production failure modes
