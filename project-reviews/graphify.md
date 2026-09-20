---
type: project-review
status: verified
maturity: active
topics: [knowledge-graph, code-intelligence, context-engineering, agents]
last_reviewed: 2026-09-20
---

# Graphify

## Evidence status

**VERIFIED FACT** for the claims explicitly attributed below to the upstream repository. Performance or token-reduction claims remain project claims until independently reproduced.

## Primary source

- Upstream repository: https://github.com/Graphify-Labs/graphify
- Historical/original repository referenced by upstream material: https://github.com/safishamsi/graphify

## Verified capabilities

According to the upstream project documentation, Graphify maps code and other project material into a queryable knowledge graph. Code extraction uses tree-sitter AST parsing; semantic material can use an AI model. The project distinguishes extracted relationships from inferred relationships and emits a persistent graph plus an interactive HTML view and report.

The current documentation explicitly positions the graph as an alternative to repeatedly searching/re-reading raw project files for structural questions.

## Outputs documented upstream

- `graph.html` — interactive graph
- `GRAPH_REPORT.md` — summarized graph findings
- `graph.json` — persistent graph

## Relevance to this Knowledge Base

Graphify is relevant to three different concerns and they must not be conflated:

1. **Code intelligence** — understanding repository structure and relationships.
2. **Context engineering** — giving coding agents structured context before raw-file exploration.
3. **Knowledge graph visualization** — human exploration of the extracted structure.

## Hypotheses to test

- **HYPOTHESIS:** Graphify can reduce unnecessary context/tool usage for architecture and dependency questions in a real project.
- **HYPOTHESIS:** Its graph can become one input to a broader engineering context layer, but it should not be assumed to represent runtime topology.
- **HYPOTHESIS:** It may be useful during VECTOR repository reconnaissance after the framework permits a controlled experiment.

## Evidence boundary

Claims such as a specific token reduction multiplier must be treated as **project-reported** until reproduced in our own benchmark.

## Planned experiment

Run the same repository-understanding tasks with and without Graphify and compare:

- task completion quality;
- files/raw content inspected;
- tool calls;
- context/token usage where measurable;
- elapsed time;
- incorrect dependency assumptions.

No adoption decision has been made.
