---
type: pattern
status: evidence-synthesized
topics: [identity, entity-resolution, provenance, graphs, epistemic-safety]
last_reviewed: 2026-09-21
---
# Evidence-Preserving Entity Resolution

## Problem
Operational intelligence often combines observations from CMDBs, telemetry, network discovery, incidents, changes and human input. Similar identifiers do not prove two observations represent the same entity.

## Pattern
1. Preserve source-declared identity and provenance.
2. Prefer exact/stable identity for canonical matching.
3. Represent uncertain equivalence as an explicit derived relation, not a destructive merge.
4. Attach basis/source and, when legitimately modeled, confidence to derived resolution.
5. Build canonical/grouped views as reversible projections.
6. Surface conflicts rather than silently choosing one observation.
7. Visually distinguish canonical relations from inferred/read-side relations.

## Safety invariant
**Similarity is not identity. Correlation is not causation. Projection is not source truth.**

## Evidence
Toise ADR 0018 documents real silent over-merge failures from tolerant matching and replaces it with exact identity. Its proposed multi-source layer preserves raw nodes and adds evidence-bearing `same_as` relations rather than fuzzy storage matching.

## Applicability
High for CMDB + OTel + incident/change graph products, service intelligence, discovery systems and agentic RCA.
