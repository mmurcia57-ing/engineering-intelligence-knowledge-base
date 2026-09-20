---
type: technology-review
status: verified
topics: [graphrag, knowledge-graph, rag]
last_reviewed: 2026-09-20
---
# GraphRAG

## Microsoft GraphRAG
Primary source: https://github.com/microsoft/graphrag

**VERIFIED FACT:** Microsoft GraphRAG is a research project for structured/hierarchical RAG. Its documentation describes extracting a knowledge graph from text, building community hierarchies and summaries, then using those structures during retrieval.

**Current lifecycle:** the upstream README states the project is largely in maintenance mode and focuses on bug/dependency/security fixes rather than new feature development.

**Operational caution:** upstream documentation warns indexing can consume substantial LLM resources.

## Neo4j GraphRAG for Python
Primary source: https://github.com/neo4j/neo4j-graphrag-python

**VERIFIED FACT:** Neo4j maintains a first-party Python GraphRAG package. It includes retrievers and knowledge-graph construction pipelines and supports graph/vector-oriented retrieval patterns.

## Decision boundary
No GraphRAG implementation has been selected for the Engineering Execution Framework.

## HYPOTHESIS
GraphRAG may improve questions requiring relationship/community context compared with plain semantic retrieval, but this must be tested against representative engineering/SRE tasks.

## Required experiment
Compare:
1. LLM-only;
2. vector RAG;
3. GraphRAG;
4. graph traversal + telemetry/context where relevant.

Measure answer quality, evidence quality, latency, indexing cost and maintenance overhead.
