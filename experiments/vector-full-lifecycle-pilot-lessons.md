# VECTOR Pilot Lessons — Product Completion Discovery

## Pilot
VECTOR brownfield full-lifecycle pilot, September 2026.

## Confirmed lessons

### 1. Closed SDD does not prove product completion
VECTOR had an unusually complete SDD baseline, implementation plan, traceability, code and tests. A separate Product Depth Gate still discovered material gaps.

Framework invariant:
`SPEC COMPLETE ≠ PRODUCT COMPLETE ≠ PRODUCTION READY`.

### 2. Minimum slices create a completion illusion
A capability can be represented by a technically valid minimum slice while remaining too thin to fulfill its Core Question for intended users.

Capability maturity should therefore be inspected as:
`ABSENT → THIN → FUNCTIONAL → ASSURED → OPERATIONAL`.

### 3. Brownfield NO-REDO must protect semantics, not every UI artifact
Valid canonical/evidence/security semantics were preserved while the experience architecture was allowed to change materially.

### 4. UX discovery must traverse the engineering chain
The useful unit of analysis was not Screen → Screenshot. It was:
`Outcome → Journey → State → Interaction → Contract → Security → Use Case → Data → Telemetry → Test → Evidence`.

### 5. Autonomous discovery needs scope discipline
The engine discovered both current-release gaps and future opportunities. Treating both as immediate implementation would create uncontrolled scope.

Required classification:
PRODUCT/UX/FUNCTIONAL/ENGINEERING/ASSURANCE/OPERABILITY GAP vs EVOLUTION-OPPORTUNITY vs EXTERNAL-DEPENDENCY.

### 6. Executable evidence changes the quality of the pilot
Adding CI exposed a real frontend behavioral-test isolation defect immediately. The defect was corrected before convergence. “Test files exist” is therefore weaker evidence than “current branch tests execute successfully.”

### 7. Local evidence must not become corporate claims
Local AuthN context, AI provider behavior, workload characterization and synthetic J02 scenarios can validate contracts and failure semantics while corporate IAM, provider/model, Source Authority and capacity remain TBD.

### 8. UX states are engineering requirements
Loading, error/retry, semantic distinctions, bounded graph focus and safe AI degradation were implemented as behavior, not presentation notes. WCAG-oriented status semantics should be executable where practical.

## Framework changes justified by pilot

- retain Product Completion Discovery Engine;
- add Product Depth Gate after specification conformance and before completion claim;
- require capability-depth and journey-closure matrices for brownfield product-completion assessments;
- require current-branch executable evidence before convergence PASS;
- treat visual redesign as permissible when UX fails mission/journey depth, while preserving valid domain invariants;
- keep evolution candidates out of implementation until promoted by controlled specification.

## Open calibration

The pilot does not yet justify numeric thresholds for “THIN” vs “FUNCTIONAL”. Keep evidence-based qualitative classification until more real projects are measured.
