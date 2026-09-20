---
type: technology-review
status: verified
topics: [mcp, agents, tools, authorization, interoperability]
last_reviewed: 2026-09-20
---
# Model Context Protocol (MCP)

## Primary source
- MCP 2026-07-28 release: https://blog.modelcontextprotocol.io/posts/2026-07-28/

## VERIFIED FACT
The 2026-07-28 MCP specification introduced a stateless protocol core, multi round-trip requests, header-based routing, cacheable list results, an extensions framework and authorization hardening.

MCP provides an interoperability layer for exposing resources/tools/capabilities to AI clients. It does not by itself define the business authorization policy or make a tool safe to execute.

## Security/architecture implications
Tool discovery, tool invocation and permission to perform the underlying business action are separate concerns.

For sensitive tools the framework must model:
- caller identity;
- authorization server/resource server boundaries;
- scopes/claims/policy;
- per-tool/action authorization;
- audit trail;
- idempotency where applicable;
- confirmation/approval for high-impact operations;
- rate/resource limits;
- safe failure and compensation where relevant.

## HYPOTHESIS
MCP can become a standardized adapter layer between engineering agents and approved enterprise capabilities, but direct write/remediation access should require deterministic governance gates.
