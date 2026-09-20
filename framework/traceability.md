# Traceability v0.2

Traceability is selective but explicit. The minimum implementation spine is:

`OUTCOME/REQ → DECISION/CONTROL → TASK → IMPLEMENTATION → TEST/CHECK → EVIDENCE`

For user-facing protected capabilities, extend when applicable:

`Outcome/Requirement → Persona/Journey → UI State → Frontend Action → API/Message Contract → Authentication Context → Authorization Policy → Backend Use Case → Domain/Data Rule → Response/Event → UI State → Telemetry/Audit → Test/Evidence`.

For quality attributes:

`Quality Goal → Measurable Scenario → Architecture Mechanism → Test/Telemetry → Evidence`.

## Rules
- stable IDs where practical;
- bidirectional navigation where useful;
- a missing applicable link is GAP/EVIDENCE-GAP, not silently ignored;
- closed decisions are immutable by default; reopening requires new evidence, impact assessment and superseding decision;
- generated artifacts must link back to source requirement/decision where feasible;
- traceability depth is proportional to risk: do not create links that provide no review/debug/change value.

## Convergence use
Convergence traverses the trace to find:
- requirement with no implementation;
- implementation with no accepted requirement;
- requirement/control with no test/evidence;
- changed contract with stale consumers/providers;
- security policy with no enforcement/test;
- architecture decision contradicted by code/deployment;
- completed task whose evidence is missing.
