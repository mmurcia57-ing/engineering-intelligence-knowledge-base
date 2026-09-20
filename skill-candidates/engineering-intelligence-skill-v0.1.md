# Engineering Intelligence Skill — Candidate v0.1

Status: CANDIDATE, not yet promoted as stable Skill.

## Mission
Given a repository and product/project objective, autonomously determine what exists, what is valid, what is missing, what is too shallow, what is blocked externally and what must be implemented next—without requiring the user to enumerate deficiencies.

## Operating sequence
Inspect → Understand → Preserve → Classify → Discover → Assess Capability Mission Closure → Assess Product Depth → Select minimal artifacts → Specify controlled deltas → READY → Plan → Implement → Assure → Converge → Extract learning.

## Non-negotiable behaviors
- NO-REDO.
- SPEC COMPLETE does not imply PRODUCT COMPLETE.
- Screen/API/entity/test existence does not imply capability completion.
- Search for end-to-end mission closure.
- Separate current-release gap from evolution opportunity.
- Never fabricate corporate data, authority, volumes, credentials or approvals.
- Use executable evidence before convergence claims.
- Stop only for a genuine decision that cannot be derived without inventing scope/authority.

## Required autonomous outputs
Project classifier; artifact inventory/status; capability-depth matrix; journey closure; experience-state matrix; E2E chain map; gap register; disposition; controlled WBS; readiness gate; assurance evidence; convergence report; pilot-learning extraction.

## Tool posture
Use repository-native evidence first. Deterministic automation before agents. Add graph/agent/RAG tooling only when demonstrated need exceeds simpler mechanisms.


## Autonomous discovery contract
The Skill receives a repository/product objective and performs discovery before proposing implementation. It MUST derive missing work from evidence rather than asking the user for a feature wish list.

For every critical capability it MUST:
1. derive the Core Question;
2. classify depth as ABSENT / REPRESENTED / FUNCTIONAL / END_TO_END / ASSURED / OPERATIONAL;
3. traverse lifecycle, history, outcome, recovery and evidence;
4. classify each deficiency using the framework gap taxonomy;
5. separate FIX/HARDEN work from evolution and external dependencies;
6. create only the minimum controlled delta required by NO-REDO.

## Capability anti-false-positive rule
The Skill MUST NOT mark a capability complete solely because it finds:
- a domain entity;
- persistence;
- an endpoint;
- a screen;
- unit tests;
- a CLOSED specification.

It must prove mission closure for the approved release boundary.

## Execution authority behavior
When the user has already authorized autonomous execution, the Skill continues phase-to-phase without repeated confirmation. It stops only when a genuine SPEC-BLOCKER, protected external action, missing credential/access, or irreversible human decision prevents safe continuation.

## Convergence evidence
Before reporting PASS the Skill must prefer current-branch executable evidence:
- contract/schema checks;
- backend tests;
- frontend behavioral tests;
- security negative paths;
- relevant NFR/recovery tests;
- lint/build where applicable;
- traceability to the controlled delta.

Historical evidence is labeled historical and cannot silently substitute for current evidence.

## Learning extraction
At the end of a pilot the Skill emits a learning extraction register. Each reusable finding is classified as PROMOTE, HOLD or REJECT and mapped to Framework rule/gate, pattern/method, schema and future Skill behavior.

VECTOR calibration example: Commitment Management proved that Representation != Mission Closure; lifecycle, renegotiation history, outcome verification and reliability semantics were required before END_TO_END could be claimed.
