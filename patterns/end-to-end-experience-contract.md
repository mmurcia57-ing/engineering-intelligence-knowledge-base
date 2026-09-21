---
type: pattern
status: decision
topics: [ux, frontend, backend, security, observability, traceability]
last_reviewed: 2026-09-21
---
# End-to-End Experience Contract

## Goal
Prevent a common failure mode: UX, frontend, API, authorization and backend behavior are designed independently and only reconciled during integration.

## Proposed traceability chain
```
Outcome / Requirement
 → Persona / Journey
 → UI State
 → Frontend Action
 → API / Message Contract
 → Authentication Context
 → Authorization Policy
 → Backend Use Case
 → Domain/Data Rule
 → Response / Event Contract
 → UI State
 → Telemetry / Audit
 → Test / Evidence
```

## Rules
1. Every critical user action must terminate in an explicit backend/domain capability or be marked prototype-only.
2. Every protected action must map to server-side authorization.
3. Every meaningful failure must have backend semantics and UX behavior.
4. Contract/schema compatibility and journey behavior require different tests.
5. Observability should allow a critical journey to be correlated across frontend/API/backend where architecture permits.
6. Evidence closes the chain; implementation alone does not.
7. Assurance must be branch-aware: an implementation branch without an executable gate is NOT ASSURED even when an equivalent historical branch has passing CI.
8. Frontend/view-model state must be checked against the actual backend contract shape; UI-only convenience fields must not silently become parallel semantics.
9. Critical continuity identifiers must be carried by the action contract when the backend already supports them; navigation-only context is not a substitute for canonical lineage.

## Pilot evidence — VECTOR
Stress-tested on VECTOR branch `experiment/vector-knowledge-rechallenge-v2` on 2026-09-21.

The contract exposed defects that screen/source review had not closed:
- the assurance workflow listened only to a historical pilot branch, leaving the active rechallenge branch without executable evidence;
- frontend evidence-quality state used convenience fields that did not match the backend `ProjectionQuality` contract;
- the backend Commitment contract already supported Service/Risk lineage, while commitment creation in the frontend omitted those identifiers;
- copy/source-token assertions failed after localization/experience evolution even when the intended behavior remained, requiring behavior/structure-oriented assurance.

After correction, the branch executed frontend tests, lint and build plus backend Maven tests through the branch-aware assurance workflow.

## Status
**DECISION — ADOPT.** The VECTOR pilot supplied executable product evidence for the pattern. Continue regression-testing it on future products; do not weaken the requirement for behavioral evidence.
