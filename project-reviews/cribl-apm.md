---
type: project-review
status: verified-source
maturity: emerging-implementation-reference
topics: [apm, service-map, incidents, warroom, investigation, traces]
last_reviewed: 2026-09-21
---
# Cribl APM

Primary source: https://github.com/criblio/apm

## VERIFIED FACT
The project documents an OpenTelemetry-powered APM experience implemented with Vite, React and TypeScript. Its product flow includes Overview, Services/Service Detail, Service Map, Traces, Logs/Metrics, Alerts & Incidents, Errors and Investigate.

Its incident model includes a war-room page with summary, investigation findings, member services and a human-annotatable timeline. The investigation flow can start from a symptom, alert or incident.

## Relevance
Especially valuable as an information-architecture reference:
`Overview → Service → Map/Trace → Incident/Warroom → Investigation`.

It also provides evidence for keeping machine investigation and human incident annotation in the same continuity chain.

## Evidence boundary
The repository is comparatively young and has low adoption signal. Treat implementation patterns as inspectable experiments, not mature-industry defaults.

## Disposition
**EXPERIMENT / ADAPT SELECTIVELY.** High conceptual fit, lower maturity weight.
