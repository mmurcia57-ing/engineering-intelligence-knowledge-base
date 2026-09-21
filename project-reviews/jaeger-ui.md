---
type: project-review
status: verified-source
maturity: mature-focused-reference
topics: [distributed-tracing, dependency-graph, timeline, flamegraph, trace-diff]
last_reviewed: 2026-09-21
---
# Jaeger UI

Primary source: https://github.com/jaegertracing/jaeger-ui

## VERIFIED FACT
Jaeger UI contains dedicated DependencyGraph, service graph, trace timeline, trace diff and trace flamegraph implementations with tests and sample datasets including larger dependency graphs.

## Relevance
A strong focused reference for progressive investigation depth:
`dependency/service relationship → trace → temporal span structure → flamegraph/diff`.

It also demonstrates that different representations answer different questions; topology, timeline and flamegraph are complementary rather than interchangeable.

## Disposition
**ADOPT REPRESENTATION-SEPARATION PRINCIPLE / ADAPT INTERACTIONS.**
