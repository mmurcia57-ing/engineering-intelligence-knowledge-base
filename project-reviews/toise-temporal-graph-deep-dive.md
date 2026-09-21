---
type: project-review
status: verified-source
maturity: emerging-architecture-reference
topics: [temporal-graph, opentelemetry, identity, provenance, topology-history]
last_reviewed: 2026-09-21
---
# Toise — temporal graph deep dive

Primary source: https://github.com/toise-dev/toise

## VERIFIED FACT
Toise models an event-backed infrastructure graph and preserves graph history. Its accepted ADR 0018 explicitly removed tolerant/fuzzy entity matching after it caused silent over-merges. Entity identity is exact and immutable; descriptive/state changes do not silently rewrite identity.

A proposed multi-source identity ADR keeps exact source observations and represents possible equivalence as non-destructive `same_as` evidence with confidence/basis/provenance, with canonical resolution as a read-side projection rather than destructive storage merge.

Its example graph client distinguishes stored relations from inferred consumer-side links; inferred links are dashed, opt-in and described as reading aids rather than canonical relations. It also shows live change events and selected-entity attributes.

## Relevance
Very strong epistemic architecture pattern for operational graphs:
- exact identity before convenience;
- source observations preserved;
- uncertain resolution represented as evidence, not silent merge;
- canonical/read model separated from raw facts;
- inferred visual links visually and semantically distinct;
- history survives current-state projection.

## Disposition
**ADOPT PRINCIPLES / ADAPT ARCHITECTURE.** Project maturity is low, so do not treat implementation scale as proven.
