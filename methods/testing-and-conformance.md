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
