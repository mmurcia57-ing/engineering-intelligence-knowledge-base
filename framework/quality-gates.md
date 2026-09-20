# Quality Gates

Quality Gates are evidence thresholds, not ceremonies. The applicable evidence is selected by project/change risk; a gate must never pass merely because a document exists.

## CONTEXT READINESS
Before delegating substantial work to an AI/human execution environment, confirm source artifacts are accessible, closed decisions are persisted, facts/hypotheses/decisions are distinct, blockers are explicit, output criteria are known and valid existing artifacts are discoverable.

## SPEC-BLOCKER
Block progression when an essential requirement, constraint, ownership decision, dependency, acceptance condition, security/privacy condition, or operational assumption is missing or contradictory. Record blocker, impact, owner/decision authority and unblock evidence.

## READY FOR PLAN
Pass when intended outcome/scope and material requirements are sufficiently understood to choose the necessary engineering artifacts without inventing missing domain facts.

## READY FOR IMPLEMENTATION
Pass only when the selected scope has sufficient evidence for its current risk profile:
- requirements and acceptance conditions are testable;
- material clarification is closed;
- necessary UX/functional behavior is represented;
- necessary architecture/data/contracts exist;
- applicable NFR quality scenarios exist;
- applicable AuthN/AuthZ/security controls are defined;
- dependencies and material risks are visible;
- observability/operability expectations are defined where applicable;
- work packages/tasks are ordered sufficiently for execution;
- validation/test evidence expected from implementation is known;
- significant decisions are recorded;
- no unresolved SPEC-BLOCKER remains.

Not every project needs every artifact. The Adaptive Artifact Selector determines applicability.

## IMPLEMENTATION ASSURANCE
A code-complete change is not automatically ready to converge. Applicable evidence may include:
- static/type/lint checks;
- unit and regression tests;
- component/integration tests;
- consumer/provider contract tests;
- architecture/conformance checks;
- security static/dependency/secret checks;
- authentication and positive/negative authorization tests;
- threat/abuse-path validation;
- selected E2E tests;
- operational/runtime verification.

Functional PASS does not imply Security PASS. Coverage percentage alone does not prove correctness.

## CONVERGENCE
Pass when accepted specification, decisions, implementation, tests and applicable quality/security/operational evidence agree sufficiently for the selected scope. Intentional deviations are recorded; accidental drift is repaired. Remaining risks are explicit.

Minimum applicable trace:
`Requirement → Implementation → Test/Check → Evidence`.

## CHANGE CONTROL
When accepted intent changes, update the authoritative requirement/specification/decision first when appropriate and propagate impact to plan, architecture, tasks, implementation, tests and evidence. Do not silently leave authoritative artifacts stale.

## PRODUCTION / RELEASE EVIDENCE
For production-impacting work, the framework selects deployment and post-deployment evidence based on risk: environment controls, approval/policy, artifact provenance, rollout/rollback, telemetry, SLI/SLO or synthetic checks, security/runtime evidence and audit trail as applicable.

## Rule
A project may use fewer gates/evidence only when the risk rationale is explicit. A project may require stronger gates when regulation, criticality, security, data sensitivity or operational blast radius warrants them.


## UX/FUNCTIONAL READY
Use when the current scope contains meaningful user interaction.

PASS when, proportional to risk and uncertainty: actor/goal is known; required journeys/tasks are covered; functional rules and material UI/system states are explicit; alternate/failure/recovery paths are addressed; IA/navigation is sufficient; data/contract needs are feasible; AuthN/AuthZ implications are known; accessibility expectations are defined; acceptance evidence is defined; and no material ambiguity is being delegated to the implementation agent.

A static mockup or happy-path screenshot alone cannot satisfy this gate for stateful software.
