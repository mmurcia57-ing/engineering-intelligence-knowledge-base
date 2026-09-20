---
type: technology-review
status: verified-synthesis
topics: [agents, memory, persistence, knowledge-graph, vector-store]
last_reviewed: 2026-09-20
---
# Agent Memory: State, Episodic Memory and Knowledge

## Primary references
- LangGraph persistence/memory: https://docs.langchain.com/oss/python/langgraph/persistence
- OpenSRE: https://github.com/swapnildahiphale/OpenSRE
- Graphify: https://github.com/safishamsi/graphify

## Separation model
Agent systems should not collapse all context into one undifferentiated "memory".

Distinguish:
1. **Execution state** — current workflow/checkpoint, deterministic continuation.
2. **Conversation/session memory** — context scoped to an interaction/thread.
3. **Episodic memory** — prior runs/incidents and their outcomes.
4. **Semantic knowledge** — durable facts/documents/entities/relationships.
5. **Operational topology** — observed runtime entities/relationships, potentially temporal.
6. **Source evidence** — immutable/retrievable provenance supporting conclusions.

## Architecture rule
Select persistence by semantics and query pattern. A vector store, graph database, relational database and workflow checkpoint store solve different problems and are not interchangeable.

## Governance
Memory requires retention, provenance, scope, access control, freshness and deletion policies. Agent-generated summaries must remain distinguishable from source evidence.

## HYPOTHESIS
A shared-memory layer can improve continuity across engineering agents, but only if namespaces, provenance and authority boundaries prevent one agent's inference from silently becoming another agent's fact.
