# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0080

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-rejuvenation-model-of-dopamine-neuron-chan-et-al-97860-model, neuroscience-other-roles-of-subthalamic-nucleus-and-dbs-in-reinforc-97972-model, neuroscience-other-single-compartment-dorsal-lateral-medium-spiny-n-150556-model, neuroscience-other-spiking-neuron-model-of-the-basal-ganglia-humphr-83559-model

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
