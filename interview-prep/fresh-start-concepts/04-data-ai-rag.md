# Data, AI, and RAG (Concept Deep Dive)

## Concept 1: Data Platform Choices

### Databricks
Strong for lakehouse engineering, ML, and advanced data processing.

### Synapse
Integrated analytics option for SQL-heavy enterprise patterns.

### Fabric
Unified SaaS analytics experience with simplified operations.

## Concept 2: Medallion Architecture

- Bronze: raw ingest
- Silver: cleansed and standardized
- Gold: business-ready curated data products

Interview expectation: explain quality gates and ownership at each layer.

## Concept 3: Batch vs Streaming

- Batch: periodic processing, lower complexity
- Streaming: near real-time decisions, more operational complexity

## Concept 4: Azure OpenAI

### Role
Managed LLM access in enterprise context.

### Interview focus
- Use case fit
- Data privacy
- Cost and latency
- Safety controls

## Concept 5: RAG (Retrieval-Augmented Generation)

### Pipeline
1. Ingestion
2. Chunking
3. Embeddings
4. Vector index
5. Retrieval and reranking
6. Prompt assembly
7. Response with citations

### Why it matters
Grounds LLM responses on enterprise data and reduces hallucinations.

## Concept 6: Prompt Injection and Data Leakage Risks

### Risks
- Malicious prompt content
- Unauthorized data access
- Sensitive output leakage

### Mitigations
- Strict retrieval filters
- Output moderation
- Context isolation
- Human review for high-risk workflows

## Concept 7: AI Evaluation

### Metrics to mention
- Groundedness
- Relevance
- Answer completeness
- Hallucination rate
- Latency and cost per request

## Concept Questions (Practice)

1. Databricks vs Synapse vs Fabric: how do you decide?
2. Why RAG instead of fine-tuning in many enterprise cases?
3. How do you reduce hallucinations in production?
4. How do you secure enterprise GenAI architecture?
5. Which quality metrics define success for GenAI systems?

