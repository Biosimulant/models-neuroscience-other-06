# Space Plan - neuroscience-general-combo-0039

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-models-for-diotic-and-dichotic-detection-davidso-126636-model, neuroscience-other-models-of-na-channels-from-a-paper-on-the-pkc-co-85112-model, neuroscience-other-models-of-vector-navigation-with-grid-cells-bush-182685-model

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
