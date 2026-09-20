---
type: pattern
status: hypothesis
topics: [framework, artifacts, no-redo, architecture, ux, security]
last_reviewed: 2026-09-20
---
# Adaptive Artifact Selector

## Goal
Generate only engineering artifacts that materially reduce uncertainty, risk or rework.

## Inputs
- criticality;
- complexity;
- uncertainty;
- integration count/type;
- data sensitivity;
- security exposure;
- operational/reliability impact;
- UX complexity;
- lifecycle/state complexity;
- deployment complexity;
- regulatory/governance constraints;
- existing valid artifacts.

## Examples
- Actors/external systems unclear → Context diagram.
- Multiple deployable units → Container view.
- Complex business process → BPMN.
- Domain discovery uncertainty → EventStorming.
- Stateful lifecycle → State Machine.
- Interaction ordering/async ambiguity → Sequence/Dynamic view.
- Significant quality target → measurable NFR scenario.
- Significant alternative/long-lived decision → ADR.
- Browser identity/security → auth/session/trust-boundary model.
- Complex permissions → authorization model/policy tests.
- External consumer/provider dependency → contract + contract tests.
- Runtime topology/operability risk → deployment/observability view.
- UX uncertainty → journey/prototype/usability test.
- Technical uncertainty → PoC/experiment.

## NO-REDO
Before creation:
`Detect existing → validate → preserve if sufficient → repair if incomplete → create only if absent`.

## Status
HYPOTHESIS pending stress test against VECTOR and at least one materially different project.
