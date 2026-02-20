# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0079

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-phase-response-curve-of-a-globus-pallidal-neuron-143100-model, neuroscience-other-rat-subthalamic-projection-neuron-gillies-and-wi-74298-model, neuroscience-other-regulation-of-firing-frequency-in-a-midbrain-dop-127507-model, neuroscience-other-regulation-of-the-firing-pattern-in-dopamine-neu-83547-model

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
