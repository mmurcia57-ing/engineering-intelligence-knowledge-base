---
type: technology-review
status: verified
topics: [openapi, json-schema, contract-testing, pact, api]
last_reviewed: 2026-09-20
---
# Frontend ↔ Backend Contract Assurance

## Primary sources
- OpenAPI Specification: https://spec.openapis.org/oas/
- JSON Schema: https://json-schema.org/
- Pact documentation/specification: https://docs.pact.io/

## VERIFIED FACT
OpenAPI provides a machine-readable API description. Schema validation can catch structural violations but is not equivalent to proving consumer/provider behavioral compatibility.

Pact defines consumer-driven contract testing: consumer tests produce concrete interaction expectations and provider verification checks that the provider satisfies them. Pact explicitly distinguishes this from a static API schema/specification.

## Assurance model
```
API description/schema
        ↓
static validation / generated types where appropriate
        ↓
consumer expectations
        ↓
provider verification
        ↓
integration tests
        ↓
critical E2E journeys
```

These layers are complementary, not substitutes.

## Framework rules
- UI capabilities must map to versioned backend contracts.
- errors are part of the contract, not incidental exceptions.
- compatibility-breaking changes require an explicit migration/version strategy.
- contract checks should run before deployment where feasible.
- critical journeys still require integration/E2E validation even when contract tests pass.

## Quality Gate candidates
- contract exists for every externally consumed endpoint/message.
- frontend assumptions are represented in schema/contract/tests.
- provider behavior is checked against published contract.
- known consumer expectations are checked.
- error/status semantics and validation behavior are tested.
- incompatible changes cannot silently pass CI.
