# Space Plan - neuroscience-general-combo-0061

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-oscillation-and-coding-in-a-proposed-nn-model-of-123986-model, neuroscience-other-oscillations-emerging-from-noise-driven-nns-tchu-168599-model, neuroscience-other-oversampling-method-to-extract-excitatory-and-in-145803-model, neuroscience-other-oxytocin-and-vip-involvement-in-prolactin-secret-91893-model

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
