# COMBO_0052 - Neuroscience General

## Scientific Question
How do general mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-neuronal-dendrite-calcium-wave-model-neymotin-et-168874-model`: Neuroscience: NeuronalDendriteCalciumWaveModelNeymotinEt168874Model
- `neuroscience-other-neuronal-morphology-goes-digital-parekh-and-asco-148644-model`: Neuroscience: NeuronalMorphologyGoesDigitalParekhAndAsco148644Model
- `neuroscience-other-neuronal-population-models-of-intracerebral-eeg-97983-model`: Neuroscience: NeuronalPopulationModelsOfIntracerebralEeg97983Model

## Wiring Rationale
- Comparative (non-causal) mode: no direct causal links were created.

## Visualization Strategy
- Monitor-driven visualization is required for this space.
- State streams are routed into explicit monitor ports (`state_a..state_d`) to avoid signal overwrite.
- At minimum, monitor visuals include one timeseries panel and one summary table.
- Rationale: A dedicated monitor model receives all participating model state streams (`state_a..state_d`) so trajectories can be compared in one place without claiming causal coupling when IO semantics are incomplete.

## Expected Behaviors
- Model output trajectories under shared runtime settings.
- Cross-model agreement/divergence in key state or metric signals.
- Relative behavior comparison without causal linkage claims.

## Known Limitations
- No new biology is introduced beyond what upstream models encode.
- Cross-model semantic matching is rule-based and may under-connect uncertain routes.

## Source Provenance
- neuroscience-other-neuronal-dendrite-calcium-wave-model-neymotin-et-168874-model :: modeldb:168874 :: https://modeldb.science/168874
- neuroscience-other-neuronal-morphology-goes-digital-parekh-and-asco-148644-model :: modeldb:148644 :: https://modeldb.science/148644
- neuroscience-other-neuronal-population-models-of-intracerebral-eeg-97983-model :: modeldb:97983 :: https://modeldb.science/97983

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
