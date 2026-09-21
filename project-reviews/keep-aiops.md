---
type: project-review
status: verified-source
maturity: mature-implementation-reference
topics: [aiops, incidents, topology, timeline, workflows, ai]
last_reviewed: 2026-09-21
---
# Keep

Primary source: https://github.com/keephq/keep

## VERIFIED FACT
Keep is an open-source AIOps/alert-management implementation. Repository inspection confirms an incident workspace with overview, alerts, activity, chat, enrichments, timeline, topology and incident-associated workflow executions. Its topology implementation uses React Flow, supports search/focus, applications/services, incident and alert context, import/export and explicit dependency editing for manual nodes.

Incident overview code exposes AI-generated summary behavior through a Copilot task while persisting a user summary separately. Incident workflows expose execution status, trigger, trigger details, start time and duration.

## Relevance
Keep materially reduces the knowledge gap between investigation and action:
`incident context → timeline/topology/evidence → human/AI interpretation → workflow execution`.

It also demonstrates a useful topology distinction: discovered/non-manual relationships can be protected while explicitly manual relationships are governed through separate mutation paths.

## Limits
Workflow execution status is not equivalent to verified operational outcome. AI-generated incident summaries are implementation evidence, not proof of correctness or epistemic safety.

## Disposition
**ADAPT / HIGH-WEIGHT REFERENCE** for incident workspace continuity, governed topology editing and investigation-to-workflow transition.
