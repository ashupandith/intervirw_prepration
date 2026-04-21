# Compute and Integration (Concept Deep Dive)

## Concept 1: App Service

### Best fit
Standard web and API hosting with low operational overhead.

### Strengths
- Managed runtime
- Built-in scaling
- Fast deployment

### Limitations
- Less deep control than AKS for complex container platforms

## Concept 2: AKS

### Best fit
Advanced containerized systems needing orchestration flexibility and deep platform control.

### Requirements
- Team maturity in Kubernetes operations
- Observability and platform tooling

### Common interview trap
Choosing AKS by default without business/operational justification.

## Concept 3: Azure Functions

### Best fit
Event-driven, short-running, burst workloads.

### Key points
- Trigger-based execution
- Consumption model
- Cold start considerations

## Concept 4: Container Apps

### Best fit
Containerized microservices with simpler operations than AKS.

### Trade-off
Less customization than AKS, but much lower platform overhead.

## Concept 5: API Management (APIM)

### Role
Central API gateway and governance layer.

### Must-know policies
- Authentication/authorization
- Rate limiting/throttling
- Request/response transformation
- Caching
- Header validation

## Concept 6: Service Bus

### Role
Reliable async messaging (queues/topics) for decoupled services.

### Must-know patterns
- Retry with exponential backoff
- Dead-letter queue
- Idempotent consumer
- Correlation IDs

## Concept 7: Event Grid

### Role
Lightweight event routing for reactive eventing.

### Good use case
Broadcast event notifications to multiple subscribers.

## Concept 8: Logic Apps

### Role
Workflow orchestration for integration-heavy business processes.

### Good use case
SaaS connector-driven workflows and approvals.

## Concept Questions (Practice)

1. App Service vs Container Apps vs AKS: decision framework?
2. Queue vs topic in Service Bus: when to use each?
3. Event Grid vs Service Bus: key differences?
4. Why APIM is needed if API already works?
5. How do you design reliable async integration end-to-end?

