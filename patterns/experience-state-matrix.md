---
type: pattern
status: hypothesis-for-pilot
version: 0.1
topics: [ux, ui-states, functional-design, assurance, traceability]
last_reviewed: 2026-09-21
---
# Experience State Matrix

## Problem
Screen inventories hide missing behavior. A polished page can still omit loading, empty, denied, stale, failure, partial and recovery behavior.

## Hypothesis
Represent important user tasks as a matrix crossing task/step with system and interaction states before implementation.

## Candidate state set
Use only applicable states:
- initial/default;
- loading;
- populated/success;
- empty/no data;
- validation error;
- system/dependency error;
- partial result;
- stale/degraded;
- permission denied;
- authentication/session transition;
- processing/long-running;
- completed;
- destructive confirmation;
- retry/recovery;
- offline/connectivity when applicable.

## Trace
`Task → State → User action → Frontend behavior → Contract/data → Policy → Backend behavior → User feedback → Telemetry → Test`

## Value to test in VECTOR
Measure whether the matrix exposes requirements/contract/test gaps that screen-only review misses, and whether its overhead is proportional to the defects/rework avoided.

Do not require the full matrix for trivial FAST changes.
