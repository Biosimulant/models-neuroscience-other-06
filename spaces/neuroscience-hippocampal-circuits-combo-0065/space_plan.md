# Space Plan - neuroscience-hippocampal-circuits-combo-0065

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-normal-ripples-abnormal-ripples-and-fast-ripples-182134-model, neuroscience-other-parvalbumin-positive-basket-cells-differentiate-153280-model, neuroscience-other-phase-precession-through-acceleration-of-local-t-143248-model, neuroscience-other-pinskyrinzelmodel-pinskyrinzelmodel-model

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
