# .NET / .NET Core Interview Notes

## What Interviewers Expect from a Senior Architect
At architect level, .NET questions are less about syntax and more about design quality, maintainability, and production readiness.

They want to know whether you can:
- design clean and scalable service architecture
- make the right API and hosting decisions
- improve performance without harming maintainability
- apply resilience, observability, and security consistently

---

## Core Concepts to Revise
### Application Design
- clean architecture and separation of concerns
- dependency injection and testability
- domain-driven boundaries where the complexity justifies it
- modularity and maintainable service composition

### API and Service Design
- RESTful API design and versioning strategy
- idempotency, validation, pagination, and error handling
- background processing with hosted services or messaging
- synchronous vs asynchronous workflows

### Performance and Reliability
- async/await and non-blocking I/O
- caching strategy
- connection handling and resource efficiency
- resilience patterns such as retries, circuit breakers, and timeouts

### Observability
- structured logging
- correlation IDs and distributed tracing
- health checks and readiness probes
- metrics and alerting alignment

---

## When to Use What
### Minimal APIs vs Controllers
**Minimal APIs are useful when:**
- the service is lightweight
- the API surface is small and straightforward
- performance and simplicity are important

**Controllers are better when:**
- the application is larger and needs clear organization
- there are many endpoints, filters, conventions, or versioning concerns
- maintainability across teams matters more than minimal ceremony

**Architect answer:**
I choose based on complexity and maintainability, not trend. For enterprise services, consistency and operational clarity often matter more than saving a few lines of code.

---

## Common Interview Questions and Sample Answers

## Q&A: Building maintainable enterprise APIs
### Q: How do you design maintainable APIs in .NET?
**Tags:** [DotNet] [API] [Architecture]

**Strong answer:**
I start with clear contracts, consistent versioning, validation, and error handling. I keep business logic out of controllers, use dependency injection for composability, and ensure the codebase is organized around clear domain or module boundaries. I also treat observability and resilience as part of the design, not something added later.

For enterprise APIs, maintainability comes from consistency, separation of concerns, and backward-compatible evolution rather than just code cleanliness.

---

## Q&A: Async programming in enterprise services
### Q: Why is async important in .NET services?
**Tags:** [DotNet] [Performance] [Architecture]

**Strong answer:**
Async is important because it helps services use resources efficiently under load, especially for I/O-heavy operations such as database calls, HTTP calls, and message processing. It improves throughput and responsiveness when applied correctly.

That said, I do not use async blindly. I focus on end-to-end flow, dependency behavior, and error handling, because incorrect async usage can increase complexity without real value.

---

## Q&A: Resilience patterns
### Q: How do you make .NET microservices resilient?
**Tags:** [DotNet] [Microservices] [Resilience]

**Strong answer:**
I use timeouts, retries with backoff, circuit breakers, idempotent handlers, and message-based decoupling where appropriate. I also make sure every dependency call is observable so failures can be diagnosed quickly.

My principle is that resilience is not only about surviving failure; it is about failing predictably and recovering safely without creating cascading impact.

---

## Real-World Example
A strong .NET enterprise service pattern is:
- ASP.NET Core API with clear contracts
- business logic separated into application/domain services
- background jobs or messaging for long-running work
- centralized exception handling and validation
- health checks, structured logs, and telemetry
- configuration and secrets externalized securely

This creates a service that is easier to scale, test, support, and evolve.

---

## Trade-Offs to Mention in Interviews
- clean architecture adds structure but can be overdone for simple services
- microservices increase flexibility but also operational overhead
- abstraction improves maintainability but too much of it can slow delivery
- performance tuning should be driven by evidence, not guesswork

---

## Mistakes to Avoid
- talking only about framework features
- ignoring versioning and backward compatibility
- tightly coupling controllers, business rules, and infrastructure
- focusing on code elegance without operational concerns
- using complex patterns where simpler modular design is enough

---

## Revision Notes
- emphasize maintainability, testability, and operational readiness
- use .NET as a business delivery platform, not just a coding topic
- always connect framework choices to performance, reliability, and team productivity
