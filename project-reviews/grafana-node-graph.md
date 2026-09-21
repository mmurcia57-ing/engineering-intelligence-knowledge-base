---
type: project-review
status: verified-source
maturity: mature-visualization-reference
topics: [grafana, node-graph, service-graph, timeline, visualization]
last_reviewed: 2026-09-21
---
# Grafana Node Graph / Service Graph

Primary source: https://github.com/grafana/grafana

## VERIFIED FACT
Grafana implements node-graph/service-graph visualization and state-timeline/flamegraph visualizations inside a composable dashboard platform. Its repository includes service-graph documentation and tested timeline/flamegraph components.

## Relevance
Useful for graph visual encoding and specialized temporal representations, but also an important architectural contrast: reusable panels are not the same thing as a persistent investigation workspace.

## Disposition
**ADAPT VISUALIZATION MECHANICS; DO NOT DEFAULT TO PANEL-COMPOSITION PRODUCT IA.**
