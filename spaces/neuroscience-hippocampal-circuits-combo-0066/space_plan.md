# Space Plan - neuroscience-hippocampal-circuits-combo-0066

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-poirazi2003-ca1pyramidalcell-poirazi2003ca1pyramidalcell-model, neuroscience-other-role-for-short-term-plasticity-and-olm-cells-in-168314-model, neuroscience-other-roles-of-i-a-and-morphology-in-ap-prop-in-ca1-py-118014-model, neuroscience-other-shaping-of-action-potentials-by-different-types-140471-model

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
