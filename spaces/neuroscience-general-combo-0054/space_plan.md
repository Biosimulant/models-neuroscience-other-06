# Space Plan - neuroscience-general-combo-0054

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-nmdar-and-gabab-kir-give-bistable-dendrites-work-169985-model, neuroscience-other-nodes-of-ranvier-with-left-shifted-nav-channels-144481-model, neuroscience-other-nodose-sensory-neuron-schild-et-al-1994-schild-a-120521-model

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
