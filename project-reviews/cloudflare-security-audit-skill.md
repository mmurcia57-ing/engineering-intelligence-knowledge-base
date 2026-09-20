---
type: project-review
status: verified
maturity: emerging
topics: [security, secure-code-review, ai-agents, skills, vulnerability-validation, unit-testing]
last_reviewed: 2026-09-20
---
# Cloudflare Security Audit Skill

## Primary source
- Repository: https://github.com/cloudflare/security-audit-skill
- Discovery source: MoureDev post/video supplied by the user.

## VERIFIED FACT
Cloudflare publishes an open-source Security Audit Skill intended to guide AI coding agents through security-focused source-code review.

The repository describes a six-phase workflow:
1. reconnaissance;
2. hunting;
3. validation;
4. verification;
5. structured output;
6. reporting.

Its purpose is to make agent security review systematic and evidence-oriented rather than a generic "look for vulnerabilities" prompt.

## Framework relevance
This exposes a gap in the current Engineering Execution Framework research: application implementation assurance must explicitly include both **correctness testing** and **security verification**.

Security review is not a substitute for unit tests, contract tests, integration tests or E2E tests. Conversely, functional tests do not prove security.

## Proposed assurance model

```
Specification / acceptance criteria
        ↓
Implementation
        ↓
Static/type/lint checks
        ↓
Unit tests
        ↓
Component/integration tests
        ↓
Contract tests
        ↓
Security verification
  ├─ SAST / dependency / secrets
  ├─ threat-informed review
  ├─ authentication tests
  ├─ authorization negative tests
  ├─ input/output validation
  └─ agent-assisted audit
        ↓
Selected E2E / abuse-path tests
        ↓
Operational verification
        ↓
Evidence / Quality Gate
```

## Unit-test framework rule
Unit tests must be derived from behavior and risk, not generated merely to increase coverage.

For changed business/domain logic, tests should cover:
- expected behavior;
- boundaries;
- invalid input;
- error/exception paths;
- state transitions;
- invariants;
- regression case when fixing a defect.

Coverage percentage is supporting evidence, not proof of correctness.

## Security rule
Security must be represented throughout the lifecycle:
`threat/requirement → architecture/control → implementation → automated test/audit → runtime evidence`.

AI security audit findings remain hypotheses until supported by code path/evidence or reproduced/validated. High-impact remediation should not be applied blindly by the same agent that proposed the finding.

## Candidate Quality Gate
A production-ready change must identify applicable evidence for:
- functional correctness;
- unit/regression testing;
- integration/contracts;
- authentication/authorization;
- application/API security;
- dependency/secrets/static analysis;
- critical abuse/failure paths;
- post-deploy/runtime verification.

## Disposition
**VERIFIED CANDIDATE — SECURITY AUDIT AGENT/SKILL.**
Evaluate during Framework v0.1 stress tests before adopting as a standard tool.
