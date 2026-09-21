---
type: project-review
status: verified-source
maturity: mature-implementation-reference
topics: [kubernetes, ebpf, service-map, traffic, drilldown, observability]
last_reviewed: 2026-09-21
---
# Pixie

Primary source: https://github.com/pixie-io/pixie

## VERIFIED FACT
Pixie is an open-source Kubernetes observability system. Its documented Live UI moves from high-level cluster state, service maps, resources and application traffic into pod state, flame graphs and individual application requests. It automatically captures supported protocol traffic and exposes service/endpoint latency, error and throughput context.

## Relevance
Strong reference for progressive disclosure:
`system/service map → service/endpoint performance → request/trace detail`.

It demonstrates that a topology surface can be a navigational entry into deeper operational evidence rather than a final visualization.

## Disposition
**ADAPT.** Preserve topology-to-evidence drill-down and traffic context; Kubernetes/eBPF collection choices are not universal product defaults.
