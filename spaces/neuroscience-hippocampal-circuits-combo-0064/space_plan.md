# Space Plan - neuroscience-hippocampal-circuits-combo-0064

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-multi-comp-ca1-o-lm-interneuron-model-with-varyi-182797-model, neuroscience-other-na-channel-mutations-in-the-dentate-gyrus-thomas-123848-model, neuroscience-other-network-model-of-the-granular-layer-of-the-cereb-50219-model, neuroscience-other-norenbergetal2010-dgbasketcell-norenbergetal2010dgbasketcell-model

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
