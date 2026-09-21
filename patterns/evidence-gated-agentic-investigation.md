---
type: pattern
status: evidence-synthesized
topics: [agentic-sre, rca, evidence, provenance, uncertainty, guardrails]
last_reviewed: 2026-09-21
---
# Evidence-Gated Agentic Investigation

## Pattern
`observation/tool result → durable evidence handle → candidate hypothesis → evidence-backed finding/verdict → report → separately governed write/action`

## Required properties
- only completed, permitted observations may become citable evidence;
- a finding must reference existing evidence;
- unresolved hypotheses remain open rather than silently becoming conclusions;
- failed/unavailable evidence collection remains visible;
- action/write authority is separate from read/investigation authority;
- human approval or explicit policy gates high-impact writes where applicable;
- the report records which actions/writes occurred after the evidence used;
- loop/budget controls prevent repeated non-progressing investigation.

## Evidence
NightWarden provides inspectable implementations for evidence IDs, citation refusal, candidate/finding records, finish gates and approved-write tracking. Existing KB references RCA-Agent, OpenSRE and evidence-first agentic RCA remain complementary.

## Boundary
This pattern improves provenance and epistemic discipline; it does not prove that an LLM conclusion is correct.

## Disposition
**ADOPT PATTERN.**
