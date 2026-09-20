---
type: method
status: verified-synthesis
version: 0.2
topics: [sdd, spec-kit, mouredev, ai-assisted-engineering, quality-gates, testing, change-control]
last_reviewed: 2026-09-20
---
# Adaptive Spec-Driven Development

## Evidence base

Primary / upstream:
- GitHub Spec Kit: https://github.github.com/spec-kit/
- GitHub Spec Kit repository: https://github.com/github/spec-kit

Practical comparison:
- MoureDev hello-sdd: https://github.com/mouredev/hello-sdd

This method is a synthesis. Neither source is adopted wholesale.

## Source workflows

### GitHub Spec Kit
Current core lifecycle:
`Specify → Plan → Tasks → Implement → Converge`.

Useful controls include clarification, checklists/cross-artifact analysis, brownfield support, spec-of-specs decomposition and convergence.

### MoureDev hello-sdd
Practical workflow:
`Constitution → Spec → Clarification → Plan → Tasks → Implementation → Validation → Change`.

Useful contributions are an explicit project constitution, visible clarification step, implementation/tests, requirement-oriented validation and explicit change handling.

## Framework SDD lifecycle

```
0. CONTEXT / CONSTITUTION
        ↓
1. INSPECT / NO-REDO
        ↓
2. SPECIFY
        ↓
3. CLARIFY
        ↓
4. PLAN + SELECT ARTIFACTS
   ├─ UX / functional model
   ├─ architecture
   ├─ data / contracts
   ├─ NFR / quality scenarios
   ├─ security / AuthN / AuthZ
   ├─ observability / operability
   └─ dependencies / delivery strategy
        ↓
5. TASKS / WORK PACKAGES
        ↓
6. READY FOR IMPLEMENTATION
        ↓
7. IMPLEMENT + ASSURE
   ├─ code
   ├─ static checks
   ├─ unit/regression tests
   ├─ component/integration tests
   ├─ contract/conformance tests
   └─ applicable security checks
        ↓
8. VALIDATE
   requirement ↔ implementation ↔ test ↔ evidence
        ↓
9. CONVERGE
        ↓
10. CHANGE / LEARN
```

## Phase rules

### 0 — Context / Constitution
Persist durable engineering constraints: project principles, mandatory standards, technology or regulatory constraints, evidence policy and non-negotiable quality rules.

Constitution is not a place for temporary feature requirements.

### 1 — Inspect / NO-REDO
Brownfield-first rule:
- discover existing specs, decisions, diagrams, contracts, code and tests;
- preserve valid artifacts;
- detect contradictions, gaps and stale evidence;
- never regenerate merely because an AI workflow has a template.

Possible statuses: `CLOSED | READY | GAP | CONFLICT | SPEC-BLOCKER | IMPLEMENTATION-GAP | EVIDENCE-GAP`.

### 2 — Specify
Describe intended behavior and acceptance conditions before implementation detail where possible.

Trace outcomes/capabilities to requirements.

### 3 — Clarify
Resolve material ambiguity before planning. Do not fabricate corporate, domain, security, data, capacity or integration facts.

Unresolved essential ambiguity becomes `SPEC-BLOCKER`.

### 4 — Plan + Adaptive Artifact Selection
Planning is not synonymous with generating every engineering document.

Use project risk/uncertainty to select only necessary artifacts. Architecture, UX, NFR, security, contracts, data, deployment and operational views are created only when they reduce material uncertainty/risk/rework.

Significant architectural choices with alternatives become ADRs.

### 5 — Tasks / Work Packages
Decompose accepted scope into traceable executable work. Maintain dependencies and distinguish work package, macro task and micro task when useful.

Dates are not invented from task count.

### 6 — READY FOR IMPLEMENTATION
Implementation starts only when the selected scope has sufficient evidence. See framework Quality Gates.

### 7 — Implement + Assure
Implementation and verification evolve together.

For changed business/domain logic, applicable unit/regression tests cover expected behavior, boundaries, invalid input, failures, state/invariants and reproduced defects.

Security assurance is independent of functional correctness. Apply risk-selected controls such as static analysis, dependency/secrets analysis, AuthN/AuthZ tests, abuse cases and validated security review.

AI-generated tests must trace to behavior/risk/defect; coverage percentage alone is not correctness.

### 8 — Validate
Validation asks whether the implemented behavior satisfies the accepted specification and quality constraints.

Minimum trace where applicable:
`Requirement → Implementation → Test/Check → Evidence`.

### 9 — Converge
Compare spec, plan, tasks, implementation, tests, security/quality evidence and operational artifacts. Record intentional deviations; repair accidental drift.

Convergence is evidence-based, not “the agent says done.”

### 10 — Change / Learn
When intent changes, update the authoritative specification/decision first when appropriate, propagate impact to architecture/tasks/tests/evidence, and preserve decision history.

Do not silently mutate implementation and leave the specification stale.

## What was adopted

| Control | Spec Kit | hello-sdd | Framework disposition |
|---|---|---|---|
| Specification before implementation | Yes | Yes | ADOPT |
| Explicit constitution | Related project principles | Explicit | ADOPT |
| Clarification | Supported | Explicit | ADOPT |
| Planning | Yes | Yes | ADOPT + expand |
| Tasks | Yes | Yes | ADOPT + dependencies/WBS |
| Implementation | Yes | Yes | ADOPT |
| Tests during implementation | Execution dependent | Explicit practical example | ADOPT + formal assurance stack |
| Validation | Convergence-oriented | Explicit | ADOPT as separate semantic check |
| Convergence | Explicit | Validation/change | ADOPT |
| Change handling | Supported by workflow evolution | Explicit | ADOPT |
| Brownfield / preserve existing | Supported | Not primary emphasis | ADOPT + NO-REDO |
| Adaptive artifact selection | Not sufficient as project framework | Not sufficient | FRAMEWORK ADDITION |
| Architecture/NFR/security/UX/contracts | Partial/tool-dependent | Example-dependent | FRAMEWORK ADDITION |
| Forecasting/capacity/dependencies | Outside core SDD | Outside core SDD | FRAMEWORK ADDITION |
| Operability/SRE/evidence governance | Outside core SDD | Outside core SDD | FRAMEWORK ADDITION |

## Non-goals

SDD is not the whole Engineering Execution Framework.
It does not replace product discovery, project classification, portfolio prioritization, forecasting, runtime reliability, governance or learning.

Spec Kit may be used as an execution harness when it fits. hello-sdd remains a practical reference, not a required tool.

## Exit evidence

An SDD cycle is complete only when applicable accepted requirements are traceable through implementation and verification evidence, convergence has resolved unintended drift, and remaining deviations/risks are explicit.
