---
type: method
status: draft-for-pilot
version: 0.1
topics: [execution, delivery-control, github-projects, dependencies, evidence, forecasting]
last_reviewed: 2026-09-20
---
# Execution Tracking & Delivery Control

## Objective
Maintain one operational view from accepted work to validated completion without creating a second planning bureaucracy.

## Control loop
`Plan → Work → Track → Detect deviation → Reforecast/Correct → Validate → Close → Learn`.

## Source-of-truth split
- Specs/architecture/ADRs/tests/code/evidence: versioned repository artifacts.
- Executable work/status/ownership/dependencies: GitHub Issues + GitHub Projects.
- Implementation changes: Pull Requests/commits.
- CI/CD evidence: checks/workflows/deployments.
- Framework gates: linked evidence; GitHub status alone is not proof.

## Work creation rule
Create a trackable Issue when the work needs at least one of:
ownership, scheduling, dependency, independent status, review, evidence or traceability.

Do not create an Issue merely to mirror every sentence of a specification.

## Work decomposition
`Capability/Epic → Feature/Work Package → Task/Subtask` as needed.

Depth is adaptive. A small FAST change may use one Issue + PR. A CRITICAL project may require work packages and separately tracked assurance/release work.

## Execution states
- Backlog — known but not selected.
- Ready — sufficiently defined for execution.
- In Progress — active execution.
- Validate — implementation exists; required validation/evidence not yet closed.
- Done — applicable acceptance/evidence complete.

Blocked is a condition, not successful progress. Use explicit dependencies and surface it visibly.

## Delivery deviation
A controller/reviewer should surface:
- overdue Target/Commitment where applicable;
- Forecast moving beyond Target/Commitment;
- blocked work;
- dependency on incomplete predecessor;
- In Progress with stale/no movement;
- implementation completed but evidence missing;
- failed Quality Gate;
- scope growth/new child work;
- reopened issue/defect;
- milestone/capability progress divergence.

Detection does not automatically imply blame or individual productivity judgment.

## Completion semantics
`Code complete ≠ Task complete ≠ Capability complete ≠ Outcome achieved`.

Done requires the evidence defined for that work. Capability progress aggregates child work but does not prove the business outcome; outcomes require their own measure/evidence.

## Forecast integration
Track TARGET, COMMITMENT, FORECAST and ACTUAL as distinct concepts. Populate only those applicable and evidence-supported. GitHub stores the data; the forecasting method defines how FORECAST is derived.

## Pilot metrics
Start small:
- open/completed work;
- blocked work;
- burn-up;
- cycle/lead-time evidence where obtainable;
- forecast variance;
- work waiting in Validate;
- rework/reopened items;
- Quality Gate failures/evidence gaps.

Do not use these as individual performance scores.

## Pilot rule
For VECTOR, first configure the minimum model and observe friction. Add fields/views/automations only when a demonstrated control question cannot be answered cleanly.
