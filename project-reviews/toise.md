---
type: project-review
status: verified
maturity: alpha
topics: [temporal-graph, opentelemetry, topology, mcp, event-sourcing]
last_reviewed: 2026-09-20
---
# Toise

## Primary source
https://github.com/toise-dev/toise

## VERIFIED FACT
Toise describes itself as an open-source backend maintaining a live queryable infrastructure graph. It ingests OpenTelemetry entity events, maintains an event-sourced bi-temporal history, and exposes the read model through GraphQL, MCP and a debug UI.

The upstream project is pre-1.0/alpha. Its README states that public contracts can still evolve.

## Architectural significance
Toise is a strong concrete reference for:
`OTel producers → entity events → durable event log → temporal graph → GraphQL/MCP → humans + agents`.

## HYPOTHESIS
A similar pattern could provide historical topology/change context for SRE and RCA. This is not an adoption decision.

## Risks / boundaries
- OpenTelemetry Entities itself is still under development.
- Toise maturity is alpha/pre-1.0.
- Upstream production-capable claims are project claims, not our independent validation.
- A temporal infrastructure graph does not replace telemetry storage, CMDB governance, or causal validation.

## Experiment
Reproduce a small topology with lifecycle changes, query current and historical state, then evaluate identity consistency and usefulness for incident/change analysis.
