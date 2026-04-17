# Integration Interview Notes

## Purpose
This file covers enterprise integration patterns, messaging, workflows, and event-driven communication.

---

## Core Concepts
- synchronous vs asynchronous integration
- queues, topics, and events
- reliability and replay handling
- idempotency and contract governance
- decoupling systems without losing visibility

---

## Sample Architect Answer
I choose the integration pattern based on business flow and failure tolerance. If the interaction needs an immediate response, synchronous APIs may be appropriate. If resilience, decoupling, or scale is more important, I prefer messaging or event-driven integration with strong monitoring and idempotency.

---

## Questions to Expand Later
- Service Bus vs Event Grid
- event-driven architecture in enterprise systems
- saga patterns and compensating actions
- integration governance and schema evolution
