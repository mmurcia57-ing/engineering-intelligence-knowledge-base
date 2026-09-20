# Autonomous Lifecycle Orchestrator v0.1

## Purpose
Turn the Engineering Intelligence Framework from a collection of methods into an executable decision sequence for brownfield and greenfield projects.

## Golden rule
The orchestrator discovers missing work from mission, approved scope, repository evidence, behavior and operating evidence. It MUST NOT require the user to enumerate deficiencies.

## Sequence
1. Context Readiness
2. Project Classification
3. Artifact/implementation inventory
4. NO-REDO reconciliation
5. Product Completion Discovery
6. Capability Mission Closure
7. Journey Closure
8. Experience State Completeness
9. E2E Engineering Chain
10. Architecture/Security/NFR/Operability fitness
11. Gap classification and disposition
12. Controlled delta specification
13. READY FOR IMPLEMENTATION
14. WBS/dependencies/execution controls
15. Implementation
16. Implementation Assurance
17. Convergence
18. Release/Operate boundary
19. Measure/Learn
20. Pilot Learning Extraction

## Autonomous loop
For each phase:
`Inspect evidence → classify state → preserve valid work → detect gaps → decide minimum justified delta → execute/produce → validate evidence → advance`.

Do not ask for permission between phases when the scope and authority are already established.

## Stop conditions
Stop only when continuing would require inventing:
- business scope or product policy;
- corporate authority/ownership;
- credentials or protected access;
- regulatory/security approval;
- production capacity/targets;
- an irreversible human decision.

Classify this as SPEC-BLOCKER or EXTERNAL-DEPENDENCY as appropriate.

## Capability mission closure
For every critical capability derive:
`Mission → Core Question → Trigger → Lifecycle → Decision → Action → Outcome → Verification → History/Return → Recovery → Evidence`.

Existence of model/API/UI/tests is insufficient.

Depth:
`ABSENT → REPRESENTED → FUNCTIONAL → END_TO_END → ASSURED → OPERATIONAL`.

## Product completion lenses
- mission completion;
- capability depth;
- journey closure;
- experience completeness;
- engineering closure;
- operational readiness.

## Engineering closure
`Outcome → Journey → UI state → Frontend action → Contract → AuthN → AuthZ → Backend use case → Domain/Data rule → Dependency/Persistence → Response/Event → UI state → Telemetry/Audit → Test → Evidence`.

## Gap taxonomy
PRODUCT-GAP, UX-GAP, FUNCTIONAL-GAP, ENGINEERING-GAP, ASSURANCE-GAP, OPERABILITY-GAP, EVOLUTION-OPPORTUNITY, EXTERNAL-DEPENDENCY, SPEC-BLOCKER.

Disposition:
FIX NOW, HARDEN NOW, SPECIFY NEXT, EXPERIMENT, EXTERNAL, REJECT/DEFER.

## Convergence rule
A convergence claim requires current-branch executable evidence for the claims that are testable. Artifact existence or historical PASS is not sufficient.

## Learning extraction rule
A pilot is not complete until reusable findings are evaluated for promotion into:
- framework rule/gate;
- pattern/method;
- schema;
- Skill behavior;
- calibration backlog.

Project-specific semantics remain project evidence, not framework law.

## VECTOR calibration
VECTOR demonstrated:
- closed SDD can still fail Product Depth;
- Commitment Management can be FUNCTIONAL while failing mission closure;
- behavior tests can reveal defects source-level tests miss;
- local security/durability/AI/NFR evidence must not become corporate claims;
- NO-REDO protects valid semantics but does not freeze weak UX.

Status: **v0.1 — validated by one brownfield pilot; requires cross-project calibration before stable v1.**
