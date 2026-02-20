# Space Plan - neuroscience-hippocampal-circuits-combo-0067

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-short-term-plasticity-at-the-cerebellar-granule-128446-model, neuroscience-other-spatial-summation-of-excitatory-and-inhibitory-i-127305-model, neuroscience-other-spiking-gridplacemap-model-pilly-and-grossberg-p-148035-model, neuroscience-other-spine-head-calcium-in-a-ca1-pyramidal-cell-model-154732-model

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
