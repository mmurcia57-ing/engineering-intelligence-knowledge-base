---
type: method
status: verified-synthesis
topics: [forecasting, critical-path, pert, monte-carlo, throughput]
last_reviewed: 2026-09-20
---
# Forecasting and Schedule Confidence

## Primary source
PMI Practice Standard for Scheduling — Third Edition:
https://www.pmi.org/standards/scheduling-third-edition

## VERIFIED FACT
PMI's scheduling standard covers critical path, PERT, rolling-wave planning and Monte Carlo simulation, including adaptive/agile scheduling contexts.

Critical path identifies the longest logical activity path and therefore the minimum modeled project duration, subject to model assumptions.

Monte Carlo schedule risk analysis runs many simulations over uncertain activity durations/risks to produce confidence information rather than one deterministic date.

## Framework forecasting model
Never let an LLM invent a completion date from task count.

Required evidence:
`remaining scope + dependencies + duration/throughput evidence + capacity + blockers/risks + uncertainty`.

Maintain:
- TARGET DATE — desired.
- COMMITMENT DATE — formally committed.
- FORECAST DATE/RANGE — evidence-based current prediction.
- ACTUAL DATE — observed completion.

## Technique selector
- CPM: dependency-driven plan with meaningful activity durations.
- PERT/three-point: uncertain activity estimates.
- Monte Carlo: uncertainty/risk distribution and confidence ranges.
- Throughput/cycle-time forecasting: repeated flow work with sufficient historical observations.
- Rolling wave: distant work is uncertain and should be elaborated progressively.

## Gate
Forecast must disclose assumptions, data window and confidence/uncertainty. Precision without evidence is prohibited.
