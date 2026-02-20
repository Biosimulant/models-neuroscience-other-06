# Space Plan - neuroscience-general-combo-0047

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-networks-of-spiking-neurons-a-review-of-tools-an-83319-model, neuroscience-other-neural-field-model-of-generalized-seizures-zhao-182906-model, neuroscience-other-neural-mass-model-based-on-single-cell-dynamics-155130-model

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
