# Operational Intelligence Implementation Matrix

Last reviewed: 2026-09-21

Purpose: compare inspectable implementations relevant to operational-intelligence products. This is reusable KB evidence, not a product-specific design.

Legend: **S** strong implementation evidence, **P** partial/specialized evidence, **—** not a primary strength of the reviewed evidence.

| Project | Topology / graph | Temporal exploration | Evidence drill-down | Incident / investigation | Action / operational continuation | Primary lesson | Disposition |
|---|---|---|---|---|---|---|---|
| Coroot | S | P | S | S | P | Evidence-backed bounded service map + incident/RCA/traces | ADAPT |
| HyperDX | S | S | S | P | — | React Flow graph from trace relations + advanced timeline mechanics | ADAPT |
| Skyhook Radar | S | S | S | S | P | Topology coordinated with Kubernetes change/event timeline | ADAPT |
| Pixie | S | P | S | P | — | Service map → endpoint/request evidence progressive disclosure | ADAPT |
| OpenObserve | P | S | S | S | P | Unified multi-signal observability and incident domain | ADAPT |
| SigNoz | P | S | S | P | — | Correlated telemetry context and temporal exploration | ADAPT |
| Jaeger UI | S | S | S | P | — | Dependency graph, trace timeline, flamegraph and diff are complementary views | ADAPT |
| Cribl APM | S | S | S | S | P | Service/map/trace → incident war-room → investigation continuity | EXPERIMENT / ADAPT |
| OneUptime | P | S | S | S | S | Detection → incident → communication → resolution/postmortem/workflow | ADAPT |
| Uptrace | S | P | S | P | — | Span-derived service graph + annotations + unified signals | ADAPT |
| Robusta | P | S | S | S | S | Alert/change correlation and remediation continuation | ADAPT |
| Caretta | S | — | P | — | — | Edges originate from observed network relationships | ADOPT PRINCIPLE |
| Grafana | S | S | S | P | P | Powerful specialized visualizations; panel composition != investigation IA | ADAPT MECHANICS |
| Perses | — | P | P | — | — | Strong dashboard/plugin architecture; useful contrast | SELECTIVE ADOPT / REJECT DASHBOARD-FIRST |

## Convergence

### Strongly recurring
1. **Evidence-backed relationships.** Service/dependency edges originate from spans, traffic, explicit topology or another identifiable source.
2. **Contextual focus.** Selection narrows or emphasizes the relevant neighborhood/evidence rather than forcing the user to restart elsewhere.
3. **Multiple coordinated representations.** Graph, timeline, trace/waterfall/flamegraph, tables and evidence panels answer different questions.
4. **Progressive disclosure.** High-level condition leads toward increasingly granular evidence.
5. **Temporal context.** Events, changes, alerts and traces need inspectable time relationships.
6. **Bounded complexity.** Filtering, focusing, aggregation, virtualization or explicit rendering limits are normal implementation concerns.

### Less consistently solved
1. Decision governance after investigation.
2. Commitment/action lifecycle tied to the original evidence.
3. Verified outcome and learning closure.
4. Explicit epistemic separation between fact, deterministic inference, AI hypothesis and human decision.

These gaps are important: they are areas where a product may legitimately differentiate rather than copy existing observability tools.

## Architectural/UX implication

A reusable operational-intelligence grammar supported by the reviewed implementations is:

```
ATTEND
  → SELECT CONTEXT
  → ORIENT SPATIALLY
  → ORIENT TEMPORALLY
  → INSPECT SOURCE EVIDENCE
  → INVESTIGATE
  → DECIDE
  → ACT
  → VERIFY OUTCOME
```

Existing OSS evidence is strongest from **ATTEND through INVESTIGATE**. Evidence for **DECIDE → ACT → VERIFY** is more fragmented across incident-management/remediation products.

## Product challenge rule

When applying this matrix to a product:
- do not select a UI because it looks futuristic;
- identify the operator decision/task;
- select the representation that exposes the required evidence;
- preserve selected context across representation changes;
- require provenance/freshness for operational relationships;
- never promote temporal association to causation without additional evidence;
- treat dashboard panels as one representation, not automatically the product shell;
- explicitly design the post-investigation path when the product owns decisions/actions/outcomes.

## Research gaps

Further research should prioritize implementations that close:
- investigation → governed decision;
- decision → commitment/action;
- action → outcome verification;
- temporal topology/history;
- large-graph interaction and accessibility;
- AI-assisted investigation with explicit provenance/uncertainty.
