---
type: technology-review
status: verified
topics: [ux, react, react-flow, cytoscape, sigma, graph-visualization]
last_reviewed: 2026-09-20
---
# Technical UI and Graph Rendering

## Primary sources
- React state guidance: https://react.dev/learn/managing-state
- React Flow performance: https://reactflow.dev/learn/advanced-use/performance
- Cytoscape.js: https://js.cytoscape.org/
- Sigma.js: https://www.sigmajs.org/

## VERIFIED FACT
React recommends modeling interfaces through explicit visual states and keeping state minimal rather than redundant.

React Flow is designed for node-based interactive UIs. Its own performance guidance highlights unnecessary re-renders as a concern with large/complex node sets and recommends memoization and collapsing large node trees.

Cytoscape.js combines interactive network visualization with graph-analysis algorithms and can also run headlessly.

Sigma.js is a WebGL-based renderer oriented to interactive large graphs and uses Graphology as its graph data model.

## Selection rule
Do not select a graph library from visual preference alone.

Evaluate:
- graph size and expected growth;
- editing vs exploration;
- graph algorithms required;
- layout complexity;
- interaction density;
- rendering technology/performance;
- accessibility/fallback strategy;
- framework integration;
- export/testing needs.

## Candidate positioning
- React Flow: workflow/node editors and application-centric interactive diagrams.
- Cytoscape.js: graph visualization plus graph-analysis requirements.
- Sigma + Graphology: large interactive exploration where WebGL scale matters.

These are candidate positions, not universal product decisions.
