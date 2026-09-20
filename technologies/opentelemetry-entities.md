---
type: technology-review
status: verified-development
topics: [opentelemetry, entities, identity, topology]
last_reviewed: 2026-09-20
---
# OpenTelemetry Entities

Primary sources:
- https://opentelemetry.io/docs/specs/otel/entities/
- https://opentelemetry.io/docs/specs/otel/entities/data-model/

## VERIFIED FACT
The OpenTelemetry Entity Data Model is currently marked **Development**.

An entity represents an object of interest associated with telemetry. The model separates identifying attributes from descriptive attributes. Entity type and identity are expected to remain stable during an entity lifetime, while descriptive attributes may change.

The specification defines principles including **Minimally Sufficient Identity** and **Repeatable Identity**. Examples include host, container, Kubernetes node/pod and service instance.

OpenTelemetry also documents Entity Events as a mechanism for communicating entity information as structured log events.

## Architectural implication
Identity is not merely a UI concern. Incorrect identity can merge distinct objects or fragment one real object into multiple graph nodes.

## HYPOTHESIS: Canonical Identity Layer
For a multi-source engineering/SRE graph, introduce an explicit identity/resolution layer before graph merge:
`source identity → canonical candidate → confidence/evidence → governed merge`.

AI may suggest matches; it must not silently merge operational entities.

## Stability boundary
Because this specification area is still under development, exact schemas/attributes must be versioned and rechecked before production adoption.
