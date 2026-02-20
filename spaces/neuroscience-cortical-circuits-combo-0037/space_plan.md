# Space Plan - neuroscience-cortical-circuits-combo-0037

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-voltage-based-stdp-synapse-clopath-et-al-2010-144566-model, neuroscience-other-vomeronasal-sensory-neuron-shimazaki-et-al-2006-64212-model, neuroscience-other-wang-buzsaki-interneuron-talathi-et-al-2010-136308-model

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
