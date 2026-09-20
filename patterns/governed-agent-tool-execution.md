---
type: pattern
status: hypothesis
topics: [agents, mcp, security, governance, authorization]
last_reviewed: 2026-09-20
---
# Governed Agent Tool Execution

## Problem
An agent can reason probabilistically while its tools may perform deterministic, high-impact external actions.

## Proposed separation
```
Agent intent / hypothesis
        ↓
Tool request
        ↓
Identity + policy + scope
        ↓
Risk / approval gate
        ↓
Deterministic validation
        ↓
Execution
        ↓
Result + audit + telemetry
        ↓
Agent interpretation
```

## Rules
- tool availability ≠ tool authorization;
- authorization is evaluated at the trusted boundary;
- destructive/high-impact operations require stronger controls than reads;
- execution evidence must be retained independently of the agent narrative;
- retries require idempotency/side-effect awareness;
- an agent cannot self-approve a control intended to constrain that same agent.

## Status
HYPOTHESIS. Candidate framework pattern informed by MCP authorization evolution, OAuth security practice and evidence-first agent architectures.
