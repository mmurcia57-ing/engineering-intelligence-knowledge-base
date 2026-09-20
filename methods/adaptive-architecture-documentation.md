---
type: method
status: verified-synthesis
topics: [c4, arc42, adr, architecture, documentation]
last_reviewed: 2026-09-20
---
# Adaptive Architecture Documentation

## Primary sources
- C4: https://c4model.com/
- arc42: https://arc42.org/documentation/

## VERIFIED FACT
C4 provides hierarchical structural views: System Context, Container, Component and Code, plus supporting Landscape, Dynamic and Deployment views. C4 explicitly says teams do not need every level; Context and Container are sufficient for many teams.

arc42 structures architecture documentation around stakeholder needs, quality requirements, runtime/deployment views, decisions, risks and other concerns. arc42 explicitly favors adequacy over excessive documentation and recommends documenting architecturally significant decisions.

## Framework synthesis
Architecture documentation should be **adaptive**.

Minimum candidate views:
- Context: actors/external systems/boundary.
- Container: major deployable/data units and responsibilities.

Add only when uncertainty/risk warrants:
- Component: internal decomposition of complex/critical containers.
- Dynamic/runtime: important interactions, error paths, async behavior.
- Deployment: infrastructure/environment affects behavior or NFRs.
- Data: identity, lineage, consistency or storage is significant.
- Security/trust: exposure/privilege/trust boundaries are significant.

## ADR rule
Create an ADR only for architecturally significant choices: structure, important quality attributes, dependencies/interfaces, risky/expensive/long-lived decisions or meaningful alternatives.

## NO-REDO alignment
A valid existing architecture view is referenced, not regenerated. A closed ADR is reopened only when new evidence or changed constraints justify supersession.
