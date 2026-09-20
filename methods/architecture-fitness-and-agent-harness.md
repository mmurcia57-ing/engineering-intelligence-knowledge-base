---
type: method
status: verified-synthesis
topics: [architecture, fitness-functions, coding-agents, quality, ci]
last_reviewed: 2026-09-20
---
# Architecture Fitness Functions and Agent Harness

## Primary references
- https://martinfowler.com/articles/devops-compliance.html
- https://martinfowler.com/articles/harness-engineering.html
- https://martinfowler.com/articles/sensors-for-coding-agents.html

## VERIFIED FACT
Fitness functions are executable checks that assess whether an implementation continues to satisfy desired architectural/quality characteristics. They can be embedded in delivery pipelines and provide repeatable evidence.

Current agent-engineering guidance distinguishes deterministic sensors (for structural properties such as dependency rules, duplication, coverage or architectural drift) from probabilistic LLM review for semantic concerns.

## Framework rule
Prefer deterministic verification wherever a requirement can be made executable. Use LLM review for semantic/judgment-heavy concerns, but do not let it replace deterministic checks that already exist.

## Harness model
`spec/constraints → implementation agent → deterministic sensors → semantic review → tests/evidence → convergence`.

## Examples
- forbidden dependency check;
- OpenAPI compatibility check;
- authz policy tests;
- performance threshold;
- accessibility checks;
- architecture dependency rules;
- security/static analysis;
- traceability/evidence completeness.

## Boundary
A passing fitness function proves only the property it measures. It does not prove whole-system correctness.
