# Handoff Master v0.1

Status: `DECISION` — baseline for review; not yet the final framework specification.

## Mission

Build a reusable, evidence-oriented engineering execution framework that reduces avoidable rework, preserves valid decisions, selects only useful artifacts and tools, and creates traceability from requirement to implementation evidence.

## Repository boundaries

- `engineering-intelligence-knowledge-base`: research, evidence, patterns, experiments, and the evolving framework.
- `VECTOR`: first application target, untouched until the framework passes review and stress tests.
- A standalone framework repository and Skill are deferred until the framework has independent lifecycle, ownership, and release needs.

## Non-negotiable principles

1. **NO-REDO RULE:** preserve valid existing work; reopen a closed decision only with new evidence or an explicit change trigger.
2. **SPEC-BLOCKER:** stop implementation when information essential to a safe decision is missing, contradictory, or unowned.
3. **READY FOR IMPLEMENTATION:** a gate, not a feeling; requirements, decisions, acceptance evidence, dependencies, risks, and required quality attributes must be sufficient for execution.
4. **Adaptive selection:** choose lifecycle, artifacts, diagrams, tools, and gates according to project class, risk, uncertainty, and change cost.
5. **Traceability:** `requirement → decision → task → code → test → evidence`.
6. **Planning honesty:** distinguish `Target Date`, `Commitment Date`, `Forecast`, and `Actual`; never invent estimates or dates.
7. **Evidence labels:** preserve `REFERENCE ≠ VERIFIED FACT ≠ HYPOTHESIS ≠ DECISION`.

## Required knowledge areas

Research covers discovery, brainstorming, prioritization, project planning, forecasting, SDD, C4/arc42, functional modeling, ADR/NFR, WBS, Quality Gates, knowledge graphs, temporal graphs, GraphRAG, entity resolution, agents, memory, MCP, Graphify, OpenTelemetry, Toise, agent observability, graph visualization, self-hosted AI, patterns, and experiments.

## Execution sequence

1. Inspect and inventory existing material.
2. Consolidate evidence and decisions without redoing closed work.
3. Verify public claims using primary sources; record unknowns as pending.
4. Draft Framework v0.x in this repository.
5. Stress-test against different project classes.
6. Apply only to a VECTOR branch after review approval.

## Explicit non-goals for v0.1

- Do not build the Skill.
- Do not modify VECTOR.
- Do not manufacture project dates, capacity, estimates, or tool validation results.
- Do not convert a reference into a fact merely because it is popular.

