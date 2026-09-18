---
name: ai-engineering
description: Design, implement, evaluate, or review production LLM, agent, semantic-search, or RAG features. Use when model behaviour, retrieval quality, tool use, safety, latency, privacy, or token cost matters.
---

# AI Engineering

Treat model output as nondeterministic and untrusted.

## Workflow

1. Define the user outcome, unacceptable failures, measurable quality bar, latency, cost, and human-oversight needs.
2. Establish a simple baseline before adding agents or complex retrieval.
3. Version prompts, model settings, tools, schemas, and retrieval configuration.
4. For RAG, evaluate parsing, chunking, metadata, embeddings, candidate retrieval, reranking, context construction, citations, and access filtering separately.
5. Enforce tenant and document permissions before content enters model context.
6. Validate structured outputs, constrain tool permissions, require confirmation for consequential actions, and defend against prompt injection and data exfiltration.
7. Build representative evaluation sets with groundedness, retrieval recall/precision, task success, refusal, safety, latency, and cost measures.
8. Add traces that connect request, retrieval, model/tool calls, versions, tokens, latency, cost, and feedback while redacting sensitive content.
9. Define fallbacks, rate limits, budget controls, and rollback of model or prompt versions.

Do not claim quality from a few demos. Report evaluation design, results, known failure classes, and operational thresholds.
