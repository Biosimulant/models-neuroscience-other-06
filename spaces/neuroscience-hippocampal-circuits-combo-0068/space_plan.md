# Space Plan - neuroscience-hippocampal-circuits-combo-0068

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-state-dependent-drug-binding-to-sodium-channels-149174-model, neuroscience-other-status-epilepticus-alters-dentate-basket-cell-to-155602-model, neuroscience-other-stochastic-calcium-mechanisms-cause-dendritic-ca-150635-model, neuroscience-other-theta-phase-precession-in-a-model-ca3-place-cell-98003-model

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
