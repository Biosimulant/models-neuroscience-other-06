# Space Plan - neuroscience-general-combo-0045

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-myelinated-nerve-fibre-myelin-resistance-depende-136296-model, neuroscience-other-neocort-pyramidal-cells-subthreshold-somatic-vol-136309-model, neuroscience-other-network-bursts-in-cultured-nn-result-from-differ-150437-model

## Wiring Plan
- Comparative mode with monitor-only routing.
- Each base model state-like output connects to monitor ports `state_a..state_d`.
- No direct causal links among base models unless explicitly upgraded later.

## Visualization Plan
- Include `StateComparisonMonitor` and `StateMetricsMonitor`.
- Require at least:
  - one timeseries visual,
  - one summary table visual.

## Validation Gates
- space schema validity
- wiring endpoint validity
- smoke run success
- repo manifest/entrypoint validators pass
