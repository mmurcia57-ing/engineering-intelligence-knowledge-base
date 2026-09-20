---
type: technology-review
status: verified
topics: [owasp, api-security, asvs, authorization, authentication]
last_reviewed: 2026-09-20
---
# Application and API Security Baseline

## Primary sources
- OWASP ASVS: https://owasp.org/projects/asvs
- OWASP API Security Project: https://owasp.org/projects/api-security-project

## VERIFIED FACT
OWASP ASVS provides verifiable technical security requirements for web applications; the current stable version referenced by OWASP is 5.0.0.

The OWASP API Security Top 10 (2023 edition currently published by the project) includes Broken Object Level Authorization, Broken Authentication, Broken Object Property Level Authorization, Broken Function Level Authorization, resource-consumption risks, sensitive business-flow exposure, SSRF, misconfiguration, inventory problems and unsafe API consumption.

## Framework implications
Authentication answers **who/what is this principal?**
Authorization answers **may this principal perform this action on this resource/context?**

Hiding UI controls is UX behavior, not an authorization enforcement point. Authorization for protected resources/actions must be enforced at the trusted server/policy boundary.

## Required threat/security artifacts are adaptive
Depending on exposure/criticality:
- trust-boundary/data-flow diagram;
- authentication/session model;
- authorization model;
- API abuse/threat cases;
- secrets/key handling;
- audit/event requirements;
- security verification requirements.

## Gate candidates
Security requirements must be testable and traceable to implementation/evidence, not merely a checklist declaration.
