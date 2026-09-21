---
type: project-review
status: verified-source
maturity: emerging-implementation-reference
topics: [agentic-sre, evidence, rca, provenance, guardrails, remediation]
last_reviewed: 2026-09-21
---
# NightWarden

Primary source: https://github.com/PrabhatMattoo/NightWarden

## VERIFIED FACT
NightWarden is an emerging SRE-agent implementation with explicit evidence bookkeeping. Repository inspection confirms:
- citable tool results receive durable evidence IDs;
- investigation findings cite only evidence IDs that correspond to answered citable calls;
- unknown/fabricated citations are refused;
- candidate hypotheses remain open until tested;
- report completeness checks detect empty records and untested candidates;
- write/remediation calls can carry explicit approval decisions;
- investigation loops have anti-loop/budget guardrails.

## Relevance
This is stronger evidence than an AI-summary pattern. It demonstrates an implementable separation between:
`tool observation → evidence handle → candidate/hypothesis → tested finding → report → gated write`.

That structure maps well to an intelligence inspector where AI output must remain traceable to source evidence and unresolved candidates remain visibly unresolved.

## Limits
Very low adoption signal and emerging maturity. Do not treat operational safety, RCA quality or remediation correctness as proven.

## Disposition
**ADOPT EPISTEMIC PATTERNS / EXPERIMENT IMPLEMENTATION IDEAS.**
