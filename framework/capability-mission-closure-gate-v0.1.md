# Capability Mission Closure Gate v0.1

## Purpose
Prevent the framework from declaring a capability complete merely because an entity, API, screen or test exists.

## Rule
**Representation is not mission closure.**

For every critical capability, derive its Core Question from product mission, approved requirements and user journeys. Then inspect whether a user can answer that question end-to-end using implemented behavior and evidence.

## Depth states
ABSENT → REPRESENTED → FUNCTIONAL → END_TO_END → ASSURED → OPERATIONAL.

- ABSENT: no meaningful implementation.
- REPRESENTED: model/API/UI exists but does not close the user mission.
- FUNCTIONAL: primary operation works, important lifecycle/journey gaps remain.
- END_TO_END: trigger through outcome/return path closes for approved scope.
- ASSURED: contracts, negative paths, NFRs and behavioral evidence exist.
- OPERATIONAL: production telemetry, support/recovery and real operating evidence exist.

## Assessment chain
Mission → Core Question → Actors/Context → Trigger → Lifecycle → Decisions → Actions → Outcome → Verification → History/Return → Failure/Recovery → Evidence.

## Mandatory tests
1. Can the intended user accomplish the capability without an undocumented manual gap?
2. Are lifecycle transitions represented, not only create/read?
3. Are historical changes reconstructable where accountability depends on them?
4. Are execution and outcome distinguished?
5. Are partial/stale/error/permission states explicit?
6. Do frontend, contract, security, backend, data and telemetry close?
7. Is the claim proven by executable/current evidence?
8. Are external dependencies separated from local gaps?
9. Does the capability answer its Core Question?
10. Would removing the UI labels still leave meaningful behavior, or is it only a representation?

Any NO prevents END_TO_END or higher unless explicitly outside approved scope.

## Brownfield behavior
Preserve valid artifacts. Do not regenerate the capability. Create only the delta required to move from observed depth to required depth.

## VECTOR evidence
Commitment Management exposed the failure mode: entity + create/list API + screen + tests existed, but renegotiation/history/outcome-pending/reliability lifecycle were not closed. The correct classification was FUNCTIONAL, not complete.
