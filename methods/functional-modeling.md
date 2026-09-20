---
type: method
status: verified-synthesis
topics: [functional-modeling, bpmn, event-storming, uml, ux]
last_reviewed: 2026-09-20
---
# Adaptive Functional Modeling

## Primary sources
- OMG BPMN 2.0.2: https://www.omg.org/spec/BPMN/
- EventStorming: https://www.eventstorming.com/

## Purpose
Functional modeling explains what the system/business does before implementation structure dominates the discussion.

## Adaptive view selector
Use the smallest view that removes material ambiguity:
- User Journey / Task Flow — user goal, touchpoints, decisions, recovery.
- BPMN — formal business/process orchestration across participants, events, gateways and activities.
- EventStorming — domain discovery around events, commands, actors, policies and boundaries.
- Use Case — actor-system behavior and alternatives.
- Activity/Flow — algorithmic or functional branching.
- State Machine — lifecycle/state-transition correctness.
- Sequence/Dynamic View — ordering across components/services.
- Data/Event Flow — movement/transformation of data or events.
- Decision Table — complex business rules/combinations.

## Rules
Do not create every diagram. Select views from uncertainty, risk and audience.
Do not mix business process, runtime deployment and data topology into one giant diagram.
Every critical alternate/error path should be represented somewhere testable.

## Traceability
`Outcome → Journey/Process → Functional Rule → Contract → Implementation → Test/Evidence`.
