---
type: technology-review
status: verified-synthesis
topics: [authorization, rbac, abac, rebac, policy]
last_reviewed: 2026-09-20
---
# Authorization Models: RBAC, ABAC and ReBAC

## Primary sources
- NIST RBAC: https://www.nist.gov/publications/role-based-access-control-rbac-features-and-motivations
- NIST SP 800-162 ABAC: https://csrc.nist.gov/pubs/sp/800/162/upd2/final
- OpenFGA authorization concepts: https://openfga.dev/docs/authorization-concepts

## VERIFIED FACT
RBAC associates permissions with roles and users with roles.
NIST ABAC evaluates attributes of subject, object, requested operation and potentially environment against policy/rules.
Relationship-based authorization derives access from relationships between subjects and resources; OpenFGA is an implementation/reference inspired by Zanzibar-style modeling.

## Selection model
RBAC: organizational responsibility is the dominant rule.
ABAC: context/attributes materially affect access.
ReBAC: ownership, membership, hierarchy or resource relationships dominate.
Hybrid: common when enterprise role + resource relationship + contextual constraints coexist.

## Framework requirements
Authorization design must identify:
`principal + resource + action + context → policy decision`.

UI visibility is never the authoritative policy enforcement point.

## Quality Gate
For critical operations, tests must cover allowed and denied cases, cross-tenant/object access, privilege boundaries and policy changes.
