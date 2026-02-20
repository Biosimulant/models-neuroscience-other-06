# Space Plan - neuroscience-general-combo-0046

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-network-model-with-dynamic-ion-concentrations-ul-144590-model, neuroscience-other-network-models-of-frequency-modulated-sweep-dete-168407-model, neuroscience-other-network-recruitment-to-coherent-oscillations-in-135903-model

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
