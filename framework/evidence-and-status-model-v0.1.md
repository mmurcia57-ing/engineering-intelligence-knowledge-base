---
type: framework-component
status: hypothesis
version: 0.1
last_reviewed: 2026-09-20
---
# Evidence and Status Model v0.1

## Knowledge classes
REFERENCE → SOURCE-VERIFIED → CLAIM-VERIFIED → HYPOTHESIS → DECISION

Additional evidence states:
PROJECT-REPORTED | REFERENCE-ONLY | UNVERIFIED | DEFERRED.

A DECISION must identify its evidence and scope. Repetition never promotes a claim.

## Execution statuses
CLOSED — accepted and no work currently required.
READY — sufficient evidence to progress.
GAP — required information/artifact/control absent.
CONFLICT — sources/artifacts disagree.
SPEC-BLOCKER — essential ambiguity/decision prevents safe progression.
IMPLEMENTATION-GAP — accepted intent not implemented.
EVIDENCE-GAP — implementation/control exists but accepted proof is absent or stale.

## Decision lifecycle
PROPOSED → ACCEPTED → SUPERSEDED.

Closed decisions are not edited into a different historical decision. New evidence creates a new/superseding record with impact.

## Evidence record minimum
ID, claim/control, source or produced artifact, timestamp/version, scope, verification method, status and links to affected requirement/decision/task/test where applicable.

## Anti-hallucination rule
If required evidence is unavailable, record UNKNOWN/TBD/GAP. Never manufacture corporate facts, architecture, volumes, dates, permissions, credentials or acceptance.
