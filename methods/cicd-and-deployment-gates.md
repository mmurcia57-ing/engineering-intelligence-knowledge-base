---
type: method
status: verified
topics: [cicd, github-actions, deployment, quality-gates]
last_reviewed: 2026-09-20
---
# CI/CD and Deployment Gates

## Primary source
GitHub deployment environments/protection rules:
https://docs.github.com/en/actions/reference/workflows-and-actions/deployments-and-environments

## VERIFIED FACT
GitHub environments can gate deployment jobs with protection rules, required reviewers, branch restrictions and custom protection rules. Environment secrets are not made available to a deployment job until applicable protection rules pass.

GitHub documents custom protection integrations with external systems such as observability, ITSM and code-quality systems.

## Framework pipeline model
`Commit/PR → build/static checks → unit/component → contract → integration/security → artifact → environment gate → deploy → post-deploy verification → evidence`.

## Rules
- gates are proportional to risk/environment;
- production promotion is distinct from build success;
- secrets are scoped to environments/workloads;
- rollback/roll-forward strategy is defined for critical changes;
- deployment evidence is linked to version/change;
- observability can participate in readiness/post-deploy validation.

## Boundary
A CI/CD platform implements gates; it does not define what “quality” means. Framework Quality Gates define criteria/evidence, pipeline tooling enforces automatable portions.
