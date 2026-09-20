# Product Completion Discovery Engine v0.1

## Purpose

Prevent the framework from confusing **specification conformance** with **product completion**.

A project may satisfy its current specification and still be incomplete because:
- the specification intentionally implemented only thin/minimum slices;
- capabilities exist nominally but lack useful depth;
- user journeys terminate before a decision/action/outcome is possible;
- UX exposes data but does not support the user's job;
- important states, integrations, controls, evidence or operational behavior remain absent;
- the current release boundary no longer matches the product mission.

The framework must discover these conditions autonomously from evidence. The user should not have to enumerate every missing feature.

## Core rule

`SPEC COMPLETE ≠ PRODUCT COMPLETE ≠ PRODUCTION READY`

These are separate claims and require separate evidence.

## Discovery model

For every project, evaluate five completion lenses.

### 1. Mission completion
Trace each declared product outcome/value proposition to executable user behavior.

Question:
> Can the target user actually achieve the promised outcome end-to-end?

A capability name, endpoint, dashboard card or passing unit test is not sufficient.

### 2. Capability depth
For every capability, classify:

- ABSENT — no usable implementation;
- THIN — minimum slice exists but does not yet satisfy the capability's core question broadly enough for intended use;
- FUNCTIONAL — useful end-to-end behavior exists for the current release boundary;
- ASSURED — functional plus behavioral/security/NFR/operability evidence;
- OPERATIONAL — production evidence exists in the target environment.

Classification must cite evidence and current release boundary.

### 3. Journey closure
For each persona/job/journey, verify:

`Trigger → Context → Understand → Decide → Act → Verify outcome → Learn/Return`

Detect dead ends, manual context reconstruction, unsupported transitions, missing feedback, missing evidence, or actions without outcome verification.

### 4. Experience completeness
Evaluate more than visual styling:

- information architecture;
- task orientation;
- navigation/context continuity;
- progressive disclosure;
- interaction feedback;
- loading/empty/partial/stale/conflict/error/permission states;
- accessibility;
- responsive behavior;
- visual hierarchy;
- cognitive load;
- explainability;
- evidence/provenance visibility;
- recoverability from failure;
- behavioral testability.

A UI can be technically implemented and still fail this lens.

### 5. Engineering closure
Verify the full chain:

`Outcome → Journey → UI state → Frontend action → Contract → AuthN → AuthZ → Backend use case → Domain/data rule → Dependency/persistence → Response/event → UI state → Telemetry/audit → Test → Evidence`

Breaks in this chain are implementation, conformance or evidence gaps.

## Autonomous gap discovery

The engine compares:
1. product mission/outcomes;
2. capability map;
3. release classification;
4. journeys/jobs;
5. current UX;
6. architecture/contracts;
7. implementation;
8. tests/evidence;
9. evolution/debt/backlog;
10. operational/release evidence.

It then emits findings without requiring the user to pre-name improvements.

## Finding types

Every discovered item MUST be classified before becoming work:

### PRODUCT-GAP
A promised current-release outcome/capability cannot be achieved sufficiently.

### UX-GAP
The behavior exists or is possible, but the experience prevents or materially impairs the user job.

### FUNCTIONAL-GAP
Required behavior or state is missing.

### ENGINEERING-GAP
Architecture/contract/security/data/observability/resilience implementation is insufficient.

### ASSURANCE-GAP
Behavior exists but evidence/testing is inadequate.

### OPERABILITY-GAP
Release/run/support/recovery/telemetry evidence is inadequate.

### EVOLUTION-OPPORTUNITY
Valuable expansion beyond the current approved release boundary. It is NOT automatically implementation scope.

### EXTERNAL-DEPENDENCY
Requires authoritative input/access outside the project.

### SPEC-BLOCKER
A contradiction or missing authoritative decision prevents safe continuation.

## Promotion rule

Discovery does not silently expand scope.

`Finding → Evidence → Classification → Impact → Current-boundary test → Disposition`

Disposition:
- FIX NOW — required to fulfill approved current product/release;
- HARDEN NOW — current behavior exists but cannot responsibly pass assurance/release;
- SPECIFY NEXT — valuable product depth requiring controlled extension;
- EXPERIMENT — uncertainty requires evidence;
- EXTERNAL — wait for authoritative dependency;
- REJECT/DEFER — insufficient value/evidence.

## Product Depth Gate

Before claiming a project/release complete, answer:

1. Are current-release product outcomes achievable by intended personas?
2. Are MUST capabilities FUNCTIONAL or better?
3. Are SHOULD capabilities either intentionally deferred or sufficiently represented?
4. Do critical journeys close through action/outcome where the mission promises it?
5. Are critical UX states represented?
6. Does the frontend/backend/security/data chain close?
7. Are critical NFRs and failure modes evidenced?
8. Are important implementation claims backed by tests/evidence?
9. Are known evolution candidates explicitly separated from current-release gaps?
10. Does the user experience communicate the product's distinctive value rather than merely exposing underlying entities?

Any NO must become a classified finding. It does not automatically block release; the current release policy determines disposition.

## Anti-patterns

The framework MUST reject:
- “all tickets closed, therefore product complete”;
- “all SDD steps closed, therefore product complete”;
- “the API exists, therefore the journey works”;
- “the screen exists, therefore UX is done”;
- “unit tests pass, therefore integration is assured”;
- “candidate backlog exists, therefore implement it”;
- asking the user to enumerate all missing product behavior before analysis.

## Brownfield rule

Preserve valid semantics and implementation, but **visual design and interaction implementation are not immutable merely because they exist**.

If the experience fails the Product Depth Gate, redesign/refactor may be justified while preserving valid domain contracts and evidence semantics.

## Output

The engine produces:
- capability-depth matrix;
- journey-closure matrix;
- experience-state matrix;
- end-to-end contract/conformance map;
- autonomous gap register;
- dispositioned remaining-work WBS;
- completion confidence statement.

## Status

v0.1 hypothesis validated initially through the VECTOR brownfield pilot. Thresholds and scoring remain intentionally non-numeric until real pilot evidence supports them.
