---
type: project-review
status: verified-source
maturity: research-prototype
topics: [rca, langgraph, mcp, telemetry, agents]
last_reviewed: 2026-09-20
---
# RCA Agent — soul-bits

Primary source: https://github.com/soul-bits/rca-agent

## VERIFIED FACT
The project describes itself as a research prototype for autonomous RCA. It receives Alertmanager events, obtains metrics/logs/traces through MCP, runs a LangGraph investigation pipeline and produces structured RCA reports.

A particularly relevant design principle is that much of the pipeline is deterministic: topology expansion, telemetry fetching/normalization, correlation, scoring, query guardrails and report structure. LLMs are used for judgment-oriented steps such as interpretation, hypothesis proposal/validation and narrative generation.

The repository explicitly requires a service map matching the target environment; it does not simply discover architecture at runtime.

## Pattern extracted
`alert → deterministic evidence collection → deterministic correlation/scope → LLM hypotheses → live-query validation → evidence-backed RCA narrative`.

## DECISION CANDIDATE
The separation **deterministic evidence first / probabilistic reasoning second** should be evaluated as a framework pattern.

## Boundary
A generated explanation is not proof of causality. Candidate causes require evidence and validation.
