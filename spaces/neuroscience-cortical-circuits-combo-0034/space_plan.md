# Space Plan - neuroscience-cortical-circuits-combo-0034

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-the-virtual-slice-setup-lytton-et-al-2008-116838-model, neuroscience-other-tight-junction-model-of-cns-myelinated-axons-dev-122442-model, neuroscience-other-tobinetal2017-tobinetal2017-model

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
