# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0078

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-multiscale-simulation-of-the-striatal-medium-spi-150284-model, neuroscience-other-nacc-medium-spiny-neuron-effects-of-cannabinoid-126640-model, neuroscience-other-nigral-dopaminergic-neurons-effects-of-ethanol-o-112359-model, neuroscience-other-optimal-deep-brain-stimulation-of-the-subthalami-93449-model

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
