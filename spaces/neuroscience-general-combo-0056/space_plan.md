# Space Plan - neuroscience-general-combo-0056

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-numerical-integration-of-izhikevich-and-hh-model-117361-model, neuroscience-other-nwbshowcase-nwbshowcase-model, neuroscience-other-odor-supported-place-cell-model-and-goal-navigat-118434-model, neuroscience-other-olfactory-bulb-granule-cell-effects-of-odor-depr-50210-model

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
