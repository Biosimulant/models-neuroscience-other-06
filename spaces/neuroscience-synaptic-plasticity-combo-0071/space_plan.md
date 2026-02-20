# Space Plan - neuroscience-synaptic-plasticity-combo-0071

## Scientific Scope
- Domain: neuroscience
- Theme: synaptic_plasticity
- Base models: neuroscience-other-oscillating-neurons-in-the-cochlear-nucleus-bahm-87454-model, neuroscience-other-oscillations-phase-of-firing-coding-and-stdp-an-123928-model, neuroscience-other-parametric-computation-and-persistent-gamma-in-a-144579-model, neuroscience-other-prob-inference-of-short-term-synaptic-plasticity-149914-model

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
