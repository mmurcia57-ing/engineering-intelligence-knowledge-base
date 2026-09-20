---
type: technology-review
status: verified
topics: [oauth, oidc, pkce, bff, browser-security]
last_reviewed: 2026-09-20
---
# Browser Authentication and Identity

## Primary sources
- RFC 10017 — OAuth 2.0 for Browser-Based Applications (IETF, August 2026): https://datatracker.ietf.org/doc/rfc10017/
- RFC 9700 — OAuth 2.0 Security Best Current Practice: https://datatracker.ietf.org/doc/html/rfc9700
- OpenID Connect Core 1.0 / approved errata: https://openid.net/wg/connect/specifications/

## VERIFIED FACT
RFC 10017 is now an IETF Best Current Practice specifically for browser-based OAuth applications. Browser public clients using Authorization Code must use PKCE; authorization servers must support/enforce it for those clients. The BCP discusses browser architectures both with and without a server-side component and their security trade-offs.

RFC 9700 requires protections against authorization-code injection and documents PKCE as required for public clients and recommended for confidential clients.

OpenID Connect is the identity/authentication layer built on OAuth 2.0; OAuth authorization and OIDC authentication must not be treated as synonyms.

## Architecture rule
Authentication architecture must be selected from client type + threat model + operational constraints, not from frontend-framework preference.

Candidate browser patterns to evaluate:
1. browser public client;
2. token-mediating backend;
3. BFF/session-oriented pattern.

## Quality Gate candidates
- Authorization Code + PKCE requirements satisfied where applicable.
- redirect URIs and CSRF defenses explicitly modeled.
- token/session storage and refresh lifecycle documented.
- logout/revocation/session expiry behavior specified.
- frontend never treats possession of UI state as authorization.
- identity provider, resource server and client trust boundaries documented.
