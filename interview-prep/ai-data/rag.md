# RAG Interview Notes

## What is RAG?
RAG, or Retrieval-Augmented Generation, combines a language model with a retrieval layer so answers are grounded in enterprise knowledge rather than only model memory.

In interviews, the important point is not the definition. It is whether you can explain how to make RAG accurate, secure, cost-effective, and production-ready.

---

## Why Enterprises Use RAG
- reduce hallucination by grounding answers in trusted content
- enable question answering over private enterprise knowledge
- improve explainability by pointing to retrieved sources
- avoid fine-tuning for every knowledge update

---

## When to Use RAG
Use RAG when:
- the answer must come from changing enterprise content
- source attribution matters
- the knowledge base is too dynamic for model-only approaches
- security and access control must be applied to documents

## When Not to Use RAG
Do not force RAG when:
- the use case is pure generation without knowledge grounding
- the content is too poor or fragmented to retrieve reliably
- the expected answer depends on transactional live systems rather than document retrieval alone

---

## Standard RAG Architecture
A practical enterprise RAG solution usually includes:
- document ingestion pipeline
- chunking and metadata enrichment
- embeddings generation
- vector or hybrid index
- retrieval orchestration
- prompt construction with grounding context
- LLM response generation
- logging, evaluation, and feedback loop

### Azure Example
- Azure Blob Storage for documents
- Azure AI Search for indexing and hybrid retrieval
- Azure OpenAI for embeddings and generation
- Functions, Logic Apps, or containerized workers for ingestion
- API Management and Entra ID for secure access
- App Insights and monitoring for observability

---

## Interview-Ready Answer
### Q: How would you design a RAG system for enterprise knowledge search?
**Tags:** [RAG] [GenAI] [AzureOpenAI] [AzureAISearch]

**Strong answer:**
I would treat RAG as both an AI problem and a platform design problem. I would start by clarifying the content types, user personas, access controls, freshness needs, and accuracy expectations. Then I would design an ingestion pipeline that cleans content, chunks it sensibly, enriches metadata, and indexes it for hybrid retrieval.

On the serving side, I would use retrieval tuned for relevance, pass only grounded context to the model, and capture citations where possible. I would also include evaluation metrics, prompt and retrieval logging, access control enforcement, and feedback loops. In enterprise settings, the success of RAG depends as much on retrieval quality and governance as on the model itself.

---

## Key Design Trade-Offs
### Chunk size
- smaller chunks improve precision
- larger chunks improve context completeness
- best choice depends on document structure and question style

### Vector vs Hybrid search
- vector search is strong for semantic similarity
- keyword search is useful for exact business terms
- hybrid search is often the best enterprise default

### Latency vs Answer Quality
- deeper retrieval and reranking improve quality
- but too many steps can slow user response times and increase cost

### Freshness vs Complexity
- near-real-time indexing improves content freshness
- but adds operational complexity and cost

---

## Risks and Mitigations
### Hallucination risk
Mitigate with grounding, limited prompt scope, citations, and response policies.

### Access control leakage
Mitigate with document-level security trimming, identity-aware retrieval, and isolated indexes where needed.

### Poor retrieval quality
Mitigate with metadata strategy, chunking optimization, hybrid search, reranking, and evaluation datasets.

### Prompt injection through documents
Mitigate with content filtering, instruction isolation, system prompt guardrails, and careful response policies.

---

## Real-World Example
A strong enterprise use case is an internal operations assistant that answers questions from architecture standards, support runbooks, SOPs, and policy documents. The value is faster knowledge access, but only if the system respects access permissions and returns grounded answers.

---

## Mistakes to Avoid
- treating RAG as only an LLM feature
- ignoring data quality and chunking strategy
- not measuring retrieval quality
- skipping access control design
- assuming a good demo equals production readiness

---

## Revision Notes
- RAG success depends on content, retrieval, and evaluation
- always mention security, grounding, and observability
- use Azure AI Search plus Azure OpenAI as a practical enterprise example
