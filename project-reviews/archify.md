---
type: project-review
status: verified
maturity: experimental
topics: [architecture, visualization, ai-assisted-engineering, skill, html, diagrams]
last_reviewed: 2026-09-20
---
# Archify — tt-ai/archify

## Primary source
- Repository: https://github.com/tt-ai/archify
- Discovery source: MoureDev video/Short supplied by the user.

## VERIFIED FACT
Archify is an open-source project that turns natural-language descriptions, codebases, infrastructure or system information into polished interactive architecture diagrams.

Its documented output is a self-contained interactive HTML artifact and it supports multiple diagram modes including architecture, workflow, state and sequence representations. The project also documents export to image/vector formats and use from AI coding environments through a reusable skill/instruction workflow.

## Why it matters to this KB
Archify is not merely a graph-rendering library. It is a candidate **architecture communication/rendering layer**:

`engineering context/spec/code → structured architectural interpretation → interactive visual artifact → review/export/presentation`.

That is materially relevant to the Framework's adaptive artifact system.

## Candidate framework role
When the Artifact Selector determines that a visual architecture/workflow/state/sequence view is necessary, Archify may be evaluated as a renderer/generator.

It must not become the source of architectural truth. Source-of-truth should remain structured/versioned engineering artifacts such as specs, architecture-as-code/diagram source, ADRs, contracts and repository evidence.

## Quality risks to test
- semantic correctness versus visual polish;
- hallucinated components/relationships;
- deterministic regeneration;
- diffability/version control;
- accessibility;
- large-system readability;
- consistency with C4/architecture conventions;
- export fidelity;
- preservation of traceability back to source evidence.

## Proposed experiment
Use the same bounded system description to generate:
1. Mermaid/C4-style source;
2. Archify interactive HTML;
3. manually reviewed expected architecture.

Measure completeness, invented elements, readability, edit/regeneration effort, export quality and traceability.

## Disposition
**VERIFIED CANDIDATE — ARCHITECTURE VISUALIZATION / COMMUNICATION.**
Do not promote to standard tool until the experiment passes.
