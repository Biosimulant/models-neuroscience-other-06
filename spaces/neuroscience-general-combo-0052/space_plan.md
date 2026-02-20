# Space Plan - neuroscience-general-combo-0052

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-neuronal-dendrite-calcium-wave-model-neymotin-et-168874-model, neuroscience-other-neuronal-morphology-goes-digital-parekh-and-asco-148644-model, neuroscience-other-neuronal-population-models-of-intracerebral-eeg-97983-model

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
