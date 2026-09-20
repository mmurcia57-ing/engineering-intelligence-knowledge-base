---
type: project-review
status: verified
topics: [dynatrace, topology, grail, dql, observability]
last_reviewed: 2026-09-20
---
# Dynatrace Smartscape on Grail

Primary sources:
- https://docs.dynatrace.com/docs/semantic-dictionary/model/smartscape
- https://docs.dynatrace.com/docs/observe/application-observability/services/services-smartscape

## VERIFIED FACT
Dynatrace documents Smartscape on Grail as its current topology model. Monitored entities are represented as nodes and relationships as edges and can be queried/traversed using DQL/Smartscape commands.

Service entities can be related through calls and connected to underlying infrastructure such as processes, containers, hosts and Kubernetes/cloud entities.

Dynatrace documentation recommends the Grail-backed Smartscape topology for new implementations rather than the Classic topology model.

## Relevance
This is a production observability reference for the pattern:
`telemetry + topology → contextual troubleshooting/traversal`.

## Boundary
Smartscape is a Dynatrace-native topology capability. Its presence does not automatically solve cross-platform canonical identity, source-of-truth governance, code knowledge, project planning or independent temporal graph requirements.

## HYPOTHESIS
Where Dynatrace already contains sufficient topology, the framework should prefer querying/reusing it over duplicating the same graph elsewhere unless a clear cross-domain or historical requirement justifies another graph.
