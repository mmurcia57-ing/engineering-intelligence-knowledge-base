---
type: project-review
status: verified-source
topics: [sre, agents, episodic-memory, knowledge-graph, incident-investigation]
last_reviewed: 2026-09-20
---
# OpenSRE

Primary source: https://github.com/swapnildahiphale/OpenSRE

## VERIFIED FACT
OpenSRE is an open-source, self-hosted AI SRE project for incident investigation. Its documented architecture uses a root investigator and specialist subagents, Neo4j for episodic memory and service-topology knowledge graph, PostgreSQL for configuration/run traces, FastAPI/SSE, and a Next.js console.

The knowledge graph is used for service dependency traversal and blast-radius context. The project documentation states investigations can continue without Neo4j if it is unavailable.

## Pattern extracted
`incident → investigator → specialist agents/skills → evidence/tools → topology KG + episodic memory → structured investigation`.

## Important distinction
Memory and topology are related but semantically different. A prior incident episode is not a service dependency edge.

## HYPOTHESIS
OpenSRE is a useful reference architecture for an enterprise agentic-SRE lab, not evidence that its exact architecture should be adopted.

## Experiment boundary
Evaluate evidence provenance, topology freshness, memory contamination, tool permissions, deterministic gates and behavior when context sources disagree.
