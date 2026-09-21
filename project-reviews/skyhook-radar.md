---
type: project-review
status: verified-source
maturity: implementation-reference
topics: [kubernetes, topology, timeline, change-intelligence, investigation]
last_reviewed: 2026-09-21
---
# Skyhook Radar

Primary source: https://github.com/skyhook-io/radar

## VERIFIED FACT
Radar is an open-source Kubernetes UI whose repository contains topology adapters/indexing, topology tests, investigation references and timeline contracts. Its documented experience combines issues, topology, an event/resource-change timeline, Helm/GitOps context, live service traffic and audits.

The timeline represents Kubernetes events and resource changes, including diffs such as replica/image changes. Topology is therefore complemented by explicit temporal/change context rather than used as a standalone visualization.

## Relevance
Strong reference for:
- topology + timeline coordination;
- change-aware operational investigation;
- resource-change diffs;
- bounded investigation references;
- combining structural and temporal context in one operator product.

## Disposition
**ADAPT.** Particularly relevant to the spatial + temporal grammar. Kubernetes-specific semantics must not be generalized into other domains without a source contract.
