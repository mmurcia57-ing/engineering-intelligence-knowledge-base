---
type: project-review
status: verified-source
maturity: mature-implementation-reference
topics: [observability, service-map, incidents, rca, topology, slo]
last_reviewed: 2026-09-21
---
# Coroot

Primary source: https://github.com/coroot/coroot

## VERIFIED FACT
Coroot is an open-source observability/APM implementation with a service map, application health, SLO monitoring, traces and incident/RCA experiences. Repository inspection confirms first-party frontend implementations for `ServiceMap.vue` and `Incident.vue`, plus backend service-map projection code.

The service map is not merely decorative: backend projection returns applications with upstream/downstream relationships, status, link weight and formatted link statistics. The UI lays applications into dependency levels, detects back-links, renders directional SVG relationships, highlights the selected service and adjacent relationships, and bounds rendering when the application count exceeds a configured threshold.

The incident experience combines incident identity/timing, application context, SLO compliance/burn-rate information, RCA state, optional propagation map, detailed analysis, immediate fixes, widgets and traces.

## Relevance to operational-intelligence products
Strong evidence for:
- topology derived from operational relationships rather than arbitrary visual proximity;
- bounded graph rendering and filtering;
- selected-node neighborhood emphasis;
- edge status/weight/context;
- incident → RCA → propagation map → traces continuity;
- SLO context inside investigation.

## Limits / evidence boundary
Coroot's implementation is evidence that these interaction/architecture patterns exist in working source code. It does not prove that its UX, RCA accuracy or topology model is optimal for another product.

## Disposition
**ADAPT.** Use as a high-weight implementation reference for service topology, bounded graph behavior and incident investigation continuity. Do not copy its page structure or treat RCA output as authoritative evidence.
