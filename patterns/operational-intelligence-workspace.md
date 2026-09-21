---
type: pattern
status: evidence-synthesized
topics: [operational-intelligence, topology, timeline, investigation, evidence, ux]
last_reviewed: 2026-09-21
---
# Operational Intelligence Workspace

## Evidence base
Synthesized from inspected/verified implementation references:
- Coroot
- OpenObserve
- Skyhook Radar
- Cribl APM
- Pixie
- Uptrace
- Caretta
- Robusta

Existing KB references such as Dynatrace Smartscape, ServiceRadar, Toise, OpenSRE and RCA Agent remain complementary evidence.

## Convergent implementation patterns

### 1. Topology is a navigation/investigation model, not decoration
Strong implementations derive relationships from operational evidence or an explicit topology model. Nodes and edges carry identity, health/condition, relationship direction or traffic/context where supported.

**Rule candidate:** visual proximity alone MUST NOT create a product relationship.

### 2. Graph scale is intentionally bounded
Coroot explicitly prevents rendering above a threshold and offers filtering. Other references scope maps to service/cluster/resource context.

**Rule candidate:** focus, filter, aggregate or progressive disclosure before rendering an unbounded graph.

### 3. Spatial and temporal context are complementary
Radar and Robusta make resource/change events temporally inspectable; Uptrace supports chart annotations; incident-oriented products preserve event sequence.

**Pattern:** selected entity/topology context should coordinate with a temporal evidence spine rather than exist as an independent graph page.

### 4. Drill-down should increase evidence resolution
Pixie moves from service map/system state toward service/endpoint/request detail. Coroot connects incident context to RCA, propagation and traces. Cribl documents service/map/trace/incident/investigation continuity.

**Pattern:** `system → service → relationship → event/trace/evidence → investigation`.

### 5. Incident/investigation is a workspace, not merely a status record
Coroot and Cribl combine incident identity with evidence, timeline/RCA/traces or human annotations. This supports a persistent investigation context.

### 6. Change association belongs in the temporal model
Radar and Robusta explicitly expose resource/application changes. Temporal adjacency is useful evidence but is not proof of causality.

### 7. Multi-signal continuity matters more than a single impressive visualization
OpenObserve, Uptrace, Pixie and Coroot all connect multiple telemetry/evidence types. A graph without a path to underlying evidence is insufficient.

## Epistemic safety
The workspace should visually distinguish:
- observed/source-backed fact;
- deterministic derived finding;
- correlation/association;
- hypothesis;
- limitation/unknown;
- governed human/system decision;
- action/commitment;
- verified outcome.

`correlation ≠ causation`
`execution completion ≠ verified outcome`
`graph projection ≠ canonical authority`

## Product-design implication
A high-ambition operational product should not be defined as either “dashboard” or “graph UI.” The stronger recurring grammar is:

`ATTEND → ORIENT SPATIALLY → ORIENT TEMPORALLY → INSPECT EVIDENCE → INVESTIGATE → DECIDE → ACT → VERIFY`

The topology, timeline and inspector are coordinated projections over the same selected context.

## Anti-patterns
- decorative network lines;
- topology disconnected from evidence;
- graph hairballs;
- KPI strip as the sole attention model;
- AI narrative presented as source fact;
- “root cause” certainty from temporal adjacency;
- context-resetting page navigation;
- invented real-time semantics;
- color-only state;
- unbounded graph rendering.

## Adoption status
**ADOPT AS KNOWLEDGE PATTERN, VALIDATE PER PRODUCT.**

This pattern is reusable knowledge, not a VECTOR-specific UI specification.
