# Space Plan - neuroscience-cortical-circuits-combo-0035

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-towards-a-virtual-c-elegans-palyanov-et-al-2012-147938-model, neuroscience-other-turtle-visual-cortex-model-nenadic-et-al-2003-wa-94845-model, neuroscience-other-updated-tritonia-swim-cpg-calin-jagemann-et-al-2-93325-model

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
