---
type: technology-review
status: verified
topics: [ux, accessibility, wcag, ui-state]
last_reviewed: 2026-09-20
---
# UX and Accessibility Baseline

## Primary sources
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- React state guidance (implementation reference): https://react.dev/learn/managing-state

## VERIFIED FACT
WCAG 2.2 is a W3C Recommendation and expresses testable, technology-independent accessibility success criteria. W3C recommends WCAG 2.2 for current/future applicability.

React's official guidance treats UI behavior as state transitions and warns that redundant/duplicate state is a common source of bugs.

## UX engineering model
A production UI specification should describe more than visual composition:
- user/persona and goal;
- journey/task flow;
- information architecture;
- states: initial/loading/empty/success/partial/error/unauthorized/offline where relevant;
- actions and permissions;
- feedback/recovery;
- accessibility behavior;
- responsive behavior;
- performance expectations;
- telemetry/evidence.

## High-density technical interfaces
Graph, dashboard and command-center interfaces additionally require:
- progressive disclosure;
- stable visual hierarchy;
- filtering/search;
- drill-down and return path;
- time/context visibility;
- provenance/freshness;
- legible failure/degraded states;
- keyboard/accessibility strategy.

## Gate candidate
A visually polished prototype is not READY if critical states, accessibility, contracts, permissions or error/recovery behavior are unspecified.
