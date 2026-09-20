---
type: pattern
status: hypothesis
topics: [rca, agents, sre, governance]
last_reviewed: 2026-09-20
---
# Evidence-first Agentic RCA

## Problem
An LLM can produce a plausible RCA narrative without proving causal relationships.

## Proposed pattern
```
Incident / Alert
      ↓
Deterministic evidence collection
      ↓
Topology + temporal scope
      ↓
Correlation / candidate generation
      ↓
LLM hypothesis formulation
      ↓
Deterministic/live-query validation
      ↓
Evidence-backed explanation
      ↓
Human/governed action
```

## Rules
1. Telemetry and change evidence precede narrative.
2. Correlation is not automatically causation.
3. Topology constrains search space; it does not prove root cause.
4. LLM hypotheses must remain distinguishable from observed facts.
5. Remediation permissions are separate from diagnostic permissions.
6. Every conclusion should preserve evidence provenance.

## Evidence basis
The pattern is informed by inspected projects such as soul-bits/rca-agent and OpenSRE, but remains a **HYPOTHESIS** until tested in our own lab.

## Proposed test
Inject a known fault into a small distributed system and compare:
- LLM-only investigation;
- telemetry RAG;
- topology-assisted investigation;
- evidence-first graph/agent investigation.
