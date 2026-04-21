# Microservices and .NET Architecture (Concept Deep Dive)

## Concept 1: Monolith vs Microservices

### Monolith
Simple deployment and easier local consistency, but hard to scale teams independently.

### Microservices
Independent deployability and team ownership, but higher distributed-system complexity.

## Concept 2: Service Boundaries

Use business capability and bounded context, not technical layers.

Interview deep dive:
- How do you split a large legacy system?
- How do you avoid chatty service calls?

## Concept 3: Data Ownership

Each service owns its data store to reduce coupling and independent release risk.

Common issue: shared database across services causing hidden coupling.

## Concept 4: Consistency Models

- Strong consistency: immediate correctness, often higher coupling
- Eventual consistency: decoupled systems, requires compensation and monitoring

## Concept 5: Outbox Pattern

Ensure reliable event publishing with transactionally recorded outbound events.

## Concept 6: Saga Pattern

Coordinate distributed business transactions via:
- Orchestration
- Choreography

## Concept 7: .NET Architecture Patterns

- Clean Architecture
- Hexagonal (Ports and Adapters)
- CQRS where justified
- Dependency Injection

## Concept 8: Observability

Must include:
- Structured logs
- Distributed tracing
- Metrics and alerting

## Concept Questions (Practice)

1. When should you not use microservices?
2. How do you define proper service boundaries?
3. How do you handle distributed transactions safely?
4. Outbox vs saga: when each is needed?
5. How do you design .NET services for testability and resilience?

