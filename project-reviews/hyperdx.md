---
type: project-review
status: verified-source
maturity: mature-implementation-reference
topics: [observability, service-map, timeline, traces, react-flow]
last_reviewed: 2026-09-21
---
# HyperDX

Primary source: https://github.com/hyperdxio/hyperdx

## VERIFIED FACT
HyperDX is an open-source observability platform unifying logs, metrics, traces, errors and session replay. Repository inspection confirms a first-class Service Map implemented with React Flow and Dagre, custom service nodes/edges, metric-aware coloring, fit-to-viewport behavior, selected-service focus and trace-scoped map support.

The service-map edges are derived from client/server trace relationships and carry request count, error percentage and latency percentiles when available. The UI explicitly reports an empty state explaining the required span relationship.

HyperDX also implements a sophisticated virtualized timeline with zoom, pan, minimap coordination and event selection.

## Relevance
Strong implementation evidence for a coordinated spatial/temporal investigation grammar:
- graph relationships derived from trace evidence;
- metric selection changes graph interpretation without changing topology truth;
- selected-service focus;
- trace-scoped topology;
- timeline zoom/pan/minimap as first-class investigation mechanics.

## Disposition
**ADAPT / HIGH-WEIGHT IMPLEMENTATION REFERENCE.**
