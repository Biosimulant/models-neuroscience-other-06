# Space Plan - neuroscience-cortical-circuits-combo-0032

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-t-channel-currents-vitko-et-al-2005-53965-model, neuroscience-other-t-type-ca-current-in-thalamic-neurons-wang-et-al-53893-model, neuroscience-other-temporal-decorrelation-by-intrinsic-cellular-dyn-84593-model

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
