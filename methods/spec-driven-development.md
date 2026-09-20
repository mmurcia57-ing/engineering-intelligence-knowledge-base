---
type: method
status: verified
topics: [sdd, spec-kit, ai-assisted-engineering, quality-gates]
last_reviewed: 2026-09-20
---
# Spec-Driven Development / GitHub Spec Kit

## Primary source
https://github.github.com/spec-kit/

## VERIFIED FACT
Current Spec Kit describes independent entry processes for SDD, bug fixing and idea assessment. Its core SDD lifecycle is:
`Specify → Plan → Tasks → Implement → Converge`.

For production-oriented work, its current guidance adds optional clarification, checklist and cross-artifact analysis quality gates. It also supports established/brownfield codebases and a spec-of-specs decomposition for work too large for one feature cycle.

## Framework integration
Spec Kit is an execution harness/candidate tool, not the entire Engineering Execution Framework.

Our framework adds concerns above and around SDD:
- problem/outcome discovery;
- evidence/research;
- adaptive artifact selection;
- UX and functional modeling;
- architecture/NFR/security;
- dependencies and forecasting;
- SRE/operability;
- traceability;
- evidence/governance;
- tool selection;
- project-level convergence.

## NO-REDO integration
When adopting SDD in an existing project:
inspect existing specs/plans/tasks/code first; preserve valid artifacts; generate only missing or contradictory artifacts.

## Gate
Do not invoke implementation merely because a spec exists. Project-specific READY criteria may require architecture, NFR, security, contracts, dependencies and acceptance/evidence to be resolved first.
