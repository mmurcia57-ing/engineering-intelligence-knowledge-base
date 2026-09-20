---
type: framework-spec
status: draft-for-stress-test
version: 0.1
last_reviewed: 2026-09-20
---
# Engineering Intelligence & Execution Framework v0.1

## Objective
Maximize useful quality in the first engineering cycle while minimizing avoidable rework and methodological overhead.

## Core principles
1. Evidence before assertion.
2. Inspect before generate.
3. NO-REDO: preserve valid artifacts and closed decisions.
4. Rigor proportional to risk and uncertainty.
5. Specification before uncontrolled implementation.
6. Deterministic controls where executable; probabilistic AI where interpretation adds value.
7. Functional correctness, security and operability are distinct assurance dimensions.
8. Trace intent through implementation to evidence.
9. Forecast from evidence; never invent dates.
10. Converge before declaring done.

## Operating lifecycle
`Intake → Classify → Context Readiness → Inspect → Frame/Specify → Clarify → Plan + Select Artifacts/Tools → Tasks/Dependencies → READY FOR IMPLEMENTATION → Implement + Assure → Validate → Converge → Release/Operate → Measure/Learn/Change`

Discovery/research/brainstorming/assessment may precede specification when the problem or solution is uncertain.

## Core engines/components
- Project Intake;
- Project Classifier;
- Artifact Detector / NO-REDO;
- Evidence & Decision Registry;
- Gap/Conflict/Blocker Analyzer;
- Adaptive Artifact Selector;
- Tool Selector;
- Adaptive SDD Engine;
- Architecture/Functional/UX/NFR/Security engines;
- Planning/WBS/Dependency/Forecasting;
- Testing & Implementation Assurance;
- Quality Gates;
- Traceability;
- Agent Governance/Harness;
- Convergence;
- Release/Operability;
- Learning/Change.

## Assurance spine
`Outcome/Requirement → Journey/Behavior → UI/Interface → Contract → AuthN/AuthZ → Backend/Domain/Data → Implementation → Test/Security Check → Telemetry/Audit → Evidence`

Only applicable links are required, but critical omissions must be explicit.

## Planning spine
`Scope → WBS → Dependencies → Remaining work → Capacity → Historical duration/throughput → Risks/blockers → Forecast`

Dates: TARGET / COMMITMENT / FORECAST / ACTUAL.

## AI execution model
`Inspect → Understand → Preserve → Detect → Decide → Produce → Verify → Evidence`

Agents do not self-authorize high-impact actions and do not convert their own narrative into proof.

## Gate spine
SOURCE INTEGRITY (knowledge baseline)
→ CONTEXT READINESS
→ READY FOR PLAN
→ READY FOR IMPLEMENTATION
→ IMPLEMENTATION ASSURANCE
→ CONVERGENCE
→ RELEASE/PRODUCTION EVIDENCE.

## Minimum sufficient engineering package
There is no fixed document count. The package is the smallest set of versioned artifacts/evidence that sufficiently controls current risk, uncertainty, implementation and operation.

## Success metrics
Candidate measures:
- Rework Rate;
- Requirements Volatility after READY;
- Architecture Changes after Implementation Start;
- First-Pass Acceptance Rate;
- Escaped Defects;
- Idea→Ready lead time;
- Ready→Production lead time;
- Decision Reversal Rate;
- percentage of SPEC-BLOCKERs discovered before implementation.

Metrics are system/process signals, not individual productivity scores.

## Current maturity
DRAFT FOR STRESS TEST. Do not call this v1.0 and do not automate it as a Skill until stress tests and a real pilot demonstrate convergence.
