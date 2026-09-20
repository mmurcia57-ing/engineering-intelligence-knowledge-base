---
type: method
status: verified-synthesis
topics: [testing, contracts, integration, e2e, architecture-conformance]
last_reviewed: 2026-09-20
---
# Testing and Conformance Strategy

## Primary references
- Pact: https://docs.pact.io/
- Martin Fowler — Test Pyramid: https://martinfowler.com/bliki/TestPyramid.html
- OpenAPI: https://spec.openapis.org/oas/

## Principle
Different tests answer different questions. Passing one layer does not imply the system is correct end-to-end.

## Assurance stack
1. Static checks — formatting/types/schema/policy.
2. Unit/component tests — local behavior.
3. Contract tests — consumer/provider expectations.
4. Integration tests — real component boundaries and infrastructure adapters.
5. Architecture/conformance checks — forbidden dependencies, boundaries, standards where automatable.
6. E2E tests — selected critical journeys through deployed/integrated system.
7. Operational verification — telemetry, SLI/SLO, synthetic/probe or production-safe evidence as applicable.

## Selection rule
Favor fast/local tests for broad coverage and reserve expensive/brittle E2E tests for high-value journeys and integration risks.

## Evidence
A Quality Gate must name the evidence it accepts. “Tests passed” without identifying scope/layer is insufficient.


## Unit and regression assurance

Unit testing is a first-class implementation gate, not an implicit sub-item.

For changed business/domain behavior, applicable tests should exercise:
- expected behavior;
- boundary conditions;
- invalid input;
- failure/exception paths;
- state transitions and invariants;
- regression reproduction for corrected defects.

Test generation by an AI agent must remain traceable to requirements, acceptance criteria, risks or a reproduced defect. Code coverage is a diagnostic signal, not sufficient evidence of correctness.

## Security assurance is orthogonal to functional testing

The assurance stack must additionally determine which security evidence applies:
- static application security analysis;
- dependency/software-composition analysis;
- secret detection;
- authentication/session tests;
- authorization positive **and negative** tests;
- input/output validation;
- API abuse cases;
- threat-informed manual or agent-assisted review;
- dynamic/runtime security verification where justified.

A functional PASS cannot imply a security PASS, and a security audit cannot imply functional correctness.

## Convergence rule for AI reviewers

Agent-reported vulnerabilities are findings/hypotheses until validated against the actual code path, configuration, dependency or reproducible behavior. The final Quality Gate records evidence and disposition, not merely the agent narrative.
