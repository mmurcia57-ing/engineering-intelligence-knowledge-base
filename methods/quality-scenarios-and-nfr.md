---
type: method
status: verified-synthesis
topics: [nfr, quality-attributes, architecture, acceptance]
last_reviewed: 2026-09-20
---
# Quality Scenarios and NFR Engineering

## Primary source
https://docs.arc42.org/section-10/

## VERIFIED FACT
arc42 recommends making quality requirements concrete and measurable through quality scenarios. A scenario can identify source, stimulus, environment, affected artifact, expected response and response measure.

## Framework pattern
Avoid vague NFRs such as:
- fast;
- scalable;
- secure;
- highly available;
- easy to use.

Prefer measurable scenario structures:
`source + stimulus + environment + artifact + response + response measure`.

## Traceability
`Quality Goal → Quality Scenario → Architecture Decision/Mechanism → Test/Telemetry → Evidence`

## Gate candidate
A critical NFR is not READY merely because it exists in prose. It needs an acceptance/evidence strategy proportionate to risk.
