# Visual Learning Diagrams

Use these diagrams to understand flow end-to-end before memorizing details.

## 1) Azure Landing Zone and Governance

```mermaid
flowchart TD
    A[Management Group Root] --> B[Platform MG]
    A --> C[Business Unit MG]
    B --> D[Shared Services Subscription]
    C --> E[Prod Subscription]
    C --> F[Non-Prod Subscription]
    E --> G[Resource Groups]
    F --> H[Resource Groups]
    A --> I[Azure Policy + RBAC Baseline]
    B --> J[Identity + Network + Monitoring Foundation]
```

## 2) Secure API and Integration Architecture

```mermaid
flowchart LR
    U[Users/Clients] --> W[WAF or Front Door]
    W --> P[API Management]
    P --> A[App Service or Container Apps]
    A --> S[Service Bus]
    S --> C[Consumer Services]
    A --> K[Key Vault via Managed Identity]
    A --> M[App Insights + Logs]
    C --> D[Data Stores via Private Endpoints]
```

## 3) Enterprise RAG Architecture

```mermaid
flowchart LR
    D[Enterprise Documents] --> I[Ingestion + Cleaning]
    I --> C[Chunking]
    C --> E[Embeddings]
    E --> V[Vector Index]
    Q[User Query] --> R[Retriever + Reranker]
    V --> R
    R --> L[LLM Prompt Assembly]
    L --> O[LLM Response with Citations]
    O --> G[Guardrails + Monitoring]
```

## Diagram Practice Questions

1. Explain each component and why it exists.
2. Identify top 3 failure points and mitigations.
3. Which parts are security-critical and why?
4. Which parts drive most operational cost?

