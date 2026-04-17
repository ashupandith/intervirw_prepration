# Rules for Storing Future Interview Questions and Answers

## Objective
This repository exists to store **senior architect-level interview material**, not generic study notes.

Every new addition should improve one or more of the following:
- clarity of interview answers
- stronger architecture thinking
- reusable enterprise examples
- leadership and stakeholder language
- concise revision value

---

## Mandatory Classification Rule
Whenever a new question is asked, classify it first.

Always identify:
1. **Primary file**
2. **Secondary file** if cross-topic
3. **Subtopic**
4. Whether to:
   - update an existing section, or
   - create a new section

Example:

```markdown
Category: Azure Architecture
File Name: core/azure.md
Subtopic: Multi-region resiliency
Store this in: core/azure.md
Cross-reference: core/security.md, interview-types/system-design.md
```

---

## Required Answer Header Format
Use this at the top of every future answer:

```markdown
Category: <category>
File Name: <primary file>
Subtopic: <subtopic>
```

Then provide:
- the architect-level answer
- store path
- cross-references

---

## Quality Rules for All Answers
### Must include
- enterprise context
- architect-level trade-offs
- decision rationale
- risks and mitigations
- practical Azure / .NET examples where relevant
- concise, interview-ready phrasing

### Must avoid
- junior developer framing
- fluffy theory without decision context
- long academic explanations
- vendor feature lists without architecture reasoning
- answers that ignore security, scalability, or operations

---

## Technical Answer Template
For technical topics, prefer this structure:
1. **What it is**
2. **Why it matters**
3. **When to use it**
4. **When not to use it**
5. **Trade-offs**
6. **Real example**
7. **Interview answer**

---

## System Design Answer Template
For architecture and system design scenarios, structure the answer as:
1. Requirements
2. Assumptions
3. Architecture
4. Scalability
5. Security
6. Observability
7. Trade-offs
8. Risks
9. Final recommendation

---

## Behavioral and Leadership Rule
Use STAR where relevant:
- **Situation**
- **Task**
- **Action**
- **Result**

For senior roles, also add:
- **Leadership lens**
- **Stakeholder impact**
- **Business outcome**

---

## Tagging Convention
Apply one or more tags to every new Q&A section.

Core tags:
- `[Azure]`
- `[DotNet]`
- `[Architecture]`
- `[Microservices]`
- `[Security]`
- `[Networking]`
- `[Integration]`
- `[API]`
- `[Data]`
- `[DevOps]`

AI / Data tags:
- `[GenAI]`
- `[RAG]`
- `[AzureOpenAI]`
- `[AzureAISearch]`
- `[Databricks]`
- `[ML]`

Interview tags:
- `[Behavioral]`
- `[SystemDesign]`
- `[Leadership]`
- `[ArchitectRole]`

---

## Naming Rule for New Q&A
### Preferred approach
Store future questions under the relevant topic file as a new subsection:

```markdown
## Q&A: <topic>
### Q: <full interview question>
**Tags:** [Azure] [Security] [ArchitectRole]
**Answer:**
```

### If a standalone file is needed
Use:

```text
YYYY-MM-topic-short-name.md
```

Examples:
- `2026-04-private-endpoints-vs-service-endpoints.md`
- `2026-04-rag-guardrails-and-evaluation.md`

---

## Cross-Reference Rule
If a question touches multiple domains, always store it in the strongest primary topic and add cross-references.

Example:
- API security question → primary in `core/security.md`
- cross-reference in `core/api-design.md`

---

## Rewrite Weak Questions Rule
If a question is too generic or junior-sounding, rewrite it into a stronger architect-level version before answering.

Example:
- Weak: *What is microservices?*
- Better: *How would you decide whether to decompose a legacy enterprise application into microservices, and what trade-offs would you evaluate?*

---

## Repository Expansion Rule
When a topic grows significantly:
- keep the main file as the summary revision sheet
- add deeper supporting notes later only if necessary
- do not duplicate the same content across multiple files

The repository should remain:
- structured
- easy to scan
- fast to revise before interviews
