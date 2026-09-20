---
type: pattern
status: hypothesis
topics: [ux, command-center, dashboards, graph, observability]
last_reviewed: 2026-09-20
---
# Progressive Disclosure for Technical Command Centers

## Problem
Dense technical interfaces can expose enough information to be impressive while making diagnosis slower.

## Proposed UX hierarchy
```
Executive / situation summary
  ↓
Domain / capability / journey
  ↓
Service / entity / incident
  ↓
Topology / timeline / evidence
  ↓
Raw telemetry / logs / traces / events
```

## Principles
- default view answers the user's current decision question;
- details are progressively revealed;
- filters/time scope remain visible;
- drill-down preserves return/context;
- status must not rely only on color;
- stale/unknown/partial data is visibly different from healthy data;
- every AI conclusion exposes provenance/evidence;
- graphs are navigation/investigation surfaces, not decorative backgrounds.

## Status
HYPOTHESIS. Requires usability/stress testing on representative SRE and executive tasks.
