# Pattern — Commitment Lifecycle Intelligence

## Problem
A commitment register easily degenerates into a CRUD list. The product mission is not to store promises; it is to preserve accountability and make execution-to-outcome reliability inspectable.

## Core question
What was committed, by which accountable organizational context, for when, what changed, what was executed, and did evidence verify the intended result?

## Required semantic separation
Commitment ≠ Action ≠ Execution completion ≠ Outcome verification.

A completed commitment can remain outcome-pending or have a persistent negative condition.

## Lifecycle requirements
- original agreement;
- accountable organizational context;
- current agreed date;
- immutable date/status history;
- renegotiation reason and time;
- distinguish pre-due renegotiation from late change;
- execution status;
- technical/risk context where applicable;
- evidence;
- action;
- outcome verification;
- return/history.

## Reliability measurement
A Commitment Reliability Rate is valid only with an explicit denominator and evaluation period. It must not become an individual productivity score.

Recommended semantic form:
fulfilled by current agreed date / commitments due in evaluated period.

Renegotiation before due date changes the current agreed date but must remain visible in history. Late renegotiation must not erase the fact that the prior commitment became overdue.

## Product-depth lesson
Entity + API + create form + list + tests = REPRESENTED/FUNCTIONAL, not necessarily END_TO_END.

The Capability Mission Closure Gate must inspect lifecycle transitions, reconstructability, outcome verification and failure/recovery before promoting the capability.

## VECTOR pilot evidence
EXT-001 supplied a valid foundation. EXT-004 was required after autonomous discovery found missing lifecycle/history/reliability depth. This is a NO-REDO extension, not a replacement.
