# Space Plan - neuroscience-general-combo-0058

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-olfactory-bulb-network-neurogenetic-restructurin-146583-model, neuroscience-other-olfactory-computations-in-mitral-granule-cell-ci-149415-model, neuroscience-other-on-stochastic-diff-eq-models-for-ion-channel-noi-128502-model, neuroscience-other-optical-stimulation-of-a-channelrhodopsin-2-posi-153196-model

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
