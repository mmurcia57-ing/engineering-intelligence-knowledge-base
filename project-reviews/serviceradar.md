---
type: project-review
status: verified-source
topics: [observability, topology, causal-analysis, graph, otel]
last_reviewed: 2026-09-20
---
# ServiceRadar

Primary reference: https://github.com/carverauto/serviceradar

## VERIFIED FACT
The GitHub repository currently points active source development/releases to the project's own code host. Its documented feature set includes distributed monitoring, topology visualization, OpenTelemetry support, graph/network discovery and a unified data layer spanning relational, time-series, vector and graph-oriented storage.

The project also documents a causal engine and blast-radius visualization. These are **upstream project claims** and have not been independently benchmarked by this KB.

## Relevance
ServiceRadar is a useful architecture/reference candidate because it combines:
- telemetry;
- topology;
- graph data;
- vector data;
- interactive visualization;
- causal-analysis claims.

## Evidence boundary
Performance claims such as very large graph rendering rates or microsecond causal isolation remain PROJECT-REPORTED until reproduced.

## HYPOTHESIS
The combination of graph topology + telemetry + causal analysis is relevant to our future SRE/RCA lab, but implementation choices must be tested independently.
