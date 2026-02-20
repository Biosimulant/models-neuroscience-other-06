# Space Plan - neuroscience-general-combo-0062

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-paired-turbulence-and-light-effect-on-calcium-in-53427-model, neuroscience-other-paradoxical-gaba-mediated-excitation-lewin-et-al-146504-model, neuroscience-other-parallel-network-simulations-with-neuron-miglior-64229-model, neuroscience-other-perturbation-sensitivity-implies-high-noise-and-144027-model

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
