# Batch and Real-Time Architecture Interview Notes

## Purpose
This file is for answering architect-level questions on batch processing, streaming, Event Hubs, Kafka-style ingestion, Structured Streaming, and low-latency analytics design.

---

## Batch vs Streaming
### Batch
- process data at scheduled intervals
- simpler and usually lower cost
- suitable when the business can tolerate delay

### Streaming or near-real-time
- process events continuously or in small micro-batches
- useful for operational alerts, live dashboards, fraud detection, and time-sensitive decisions
- adds complexity and cost, so it should be justified by business value

---

## Decision Rule
I do not recommend streaming unless the business truly benefits from lower latency. Many organizations ask for real-time when near-real-time or frequent batch is actually enough.

---

## Azure Pattern for Real-Time Ingestion
A practical Azure design often includes:
- Event Hubs or Kafka-compatible ingestion
- Stream processing with Databricks Structured Streaming or other processing engines
- curated serving layer for dashboards and analytics
- monitoring, replay strategy, and dead-letter handling

---

## Late and Out-of-Order Events
You handle these with:
- watermarking
- event-time logic
- deduplication strategy
- replay-safe pipeline design

---

## Common Interview Questions
- What is the difference between batch and streaming architectures?
- When should near-real-time be used instead of batch?
- How do you design a real-time ingestion architecture on Azure?
- What is Structured Streaming?
- How do you handle late-arriving and out-of-order events?

---

## Strong Sample Answer
### Q: How do you decide whether the business really needs streaming?
**Tags:** [Data] [Streaming] [Architecture]

**Answer:**
I start with the decision latency the business actually needs. If the action can wait for hourly or even fifteen-minute updates, I prefer a simpler and cheaper batch or micro-batch design. I recommend streaming only when lower latency creates measurable business value such as fraud detection, operational alerting, or live customer experience improvements.
