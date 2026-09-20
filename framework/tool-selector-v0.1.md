---
type: framework-component
status: hypothesis
version: 0.1
last_reviewed: 2026-09-20
---
# Tool Selector v0.1

## Principle
Choose tools from an engineering need, never from novelty.

`Need → Required capability → Method/pattern → Candidates → Evidence → Experiment if needed → Decision → ADR/standard when significant`

## Evaluation dimensions
Functionality, maturity, interoperability, automation, security, observability, maintainability, portability/lock-in, operating complexity, cost/licensing, team fit, evidence quality and exit strategy.

## Candidate mapping
- specification: Markdown/Git + Spec Kit when useful;
- architecture source: Mermaid / PlantUML / Structurizr / D2 as appropriate;
- architecture communication: Archify candidate after experiment;
- process: BPMN.io / Mermaid / draw.io according to formality;
- interactive node editors: React Flow;
- algorithmic graph analysis: Cytoscape.js;
- large graph rendering: Sigma.js + Graphology candidate;
- design/prototyping: Figma/Penpot;
- delivery/evidence: GitHub issues/projects/actions/environments;
- agent interoperability: MCP when tool interoperability is actually required;
- stateful agent orchestration: LangGraph candidate only for state/branching/persistence/HITL;
- automation: deterministic workflow engine/code before adding agentic orchestration;
- knowledge graph/GraphRAG: only after retrieval/relationship need is demonstrated.

## Rules
A tool appearing in research is not selected by default.
Prefer existing organizational capability when it satisfies the requirement.
A new tool with material lock-in/security/operational impact requires explicit decision evidence.
PoC results are evidence, not automatic adoption.
