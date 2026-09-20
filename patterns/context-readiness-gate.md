---
type: quality-pattern
status: hypothesis
topics: [delegation, agents, context, evidence, quality-gates]
last_reviewed: 2026-09-20
---
# Context Readiness Gate

## Problem
Delegating a context-heavy task to an agent/Work/coding tool before evidence and decisions are materialized causes rediscovery, invention and rework.

## PASS criteria
Before delegation:
- required source artifacts are identifiable and accessible;
- relevant closed decisions are persisted;
- VERIFIED FACT / HYPOTHESIS / DECISION are distinguishable;
- unresolved blockers are explicit;
- output/completeness criteria are defined;
- the delegate can access the required repository/files/tools;
- existing valid artifacts are discoverable to preserve NO-REDO.

## Result
PASS → delegate execution.
FAIL → materialize missing context first.

## Evidence basis
This pattern was derived from the KB recovery itself: scaffolding without the underlying corpus was insufficient for reliable consolidation. It remains a framework candidate until tested across additional projects.
