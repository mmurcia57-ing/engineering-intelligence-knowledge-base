---
type: framework-component
status: hypothesis
version: 0.1
last_reviewed: 2026-09-20
---
# Project Classifier v0.1

## Purpose
Select proportional engineering rigor. Classification never replaces domain judgment and never lowers mandatory regulatory/security controls.

## Dimensions
Assess each as LOW / MEDIUM / HIGH / UNKNOWN:
- business/operational criticality;
- technical complexity;
- requirement/solution uncertainty;
- integration/dependency complexity;
- data sensitivity;
- security/exposure;
- scale/performance;
- reliability/availability impact;
- UX/journey complexity;
- regulatory/governance impact;
- reversibility/blast radius;
- brownfield/change complexity.

UNKNOWN is not LOW. Material UNKNOWN may trigger research, experiment or SPEC-BLOCKER.

## Profiles
### FAST
Low-risk, bounded, reversible work with understood behavior and dependencies. Collapse phases and minimize artifacts, but retain traceability and applicable tests.

### STANDARD
Normal product/application work with meaningful integration, UX, data or operational concerns. Use full lifecycle selectively.

### CRITICAL
High criticality, sensitive data/security, regulatory exposure, large blast radius or demanding reliability. Stronger architecture, threat/security, NFR, deployment, evidence and approval controls.

### EXPERIMENTAL
Material uncertainty about feasibility/solution/value. Optimize first for learning through research/PoC/prototype. Do not pretend experimental evidence is production readiness.

Profiles may combine: e.g. CRITICAL + EXPERIMENTAL.

## Escalation rules
- Any mandatory legal/regulatory control overrides profile simplification.
- High security/data exposure cannot be downgraded by low implementation size.
- High blast radius/reversibility concern strengthens release controls.
- Unknown essential facts are surfaced, not guessed.
- Reclassify when evidence materially changes.

## Output
Classification record contains dimensions, evidence, profile, rationale, mandatory controls and unresolved unknowns.
