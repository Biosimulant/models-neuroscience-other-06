# COMBO_0067 - Neuroscience Hippocampal Circuits

## Scientific Question
How do recurrent hippocampal motifs shape network dynamics over time?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-short-term-plasticity-at-the-cerebellar-granule-128446-model`: Neuroscience: ShortTermPlasticityAtTheCerebellarGranule128446Model
- `neuroscience-other-spatial-summation-of-excitatory-and-inhibitory-i-127305-model`: Neuroscience: SpatialSummationOfExcitatoryAndInhibitoryI127305Model
- `neuroscience-other-spiking-gridplacemap-model-pilly-and-grossberg-p-148035-model`: Neuroscience: SpikingGridplacemapModelPillyAndGrossbergP148035Model
- `neuroscience-other-spine-head-calcium-in-a-ca1-pyramidal-cell-model-154732-model`: Neuroscience: SpineHeadCalciumInACa1PyramidalCellModel154732Model

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
- neuroscience-other-short-term-plasticity-at-the-cerebellar-granule-128446-model :: modeldb:128446 :: https://modeldb.science/128446
- neuroscience-other-spatial-summation-of-excitatory-and-inhibitory-i-127305-model :: modeldb:127305 :: https://modeldb.science/127305
- neuroscience-other-spiking-gridplacemap-model-pilly-and-grossberg-p-148035-model :: modeldb:148035 :: https://modeldb.science/148035
- neuroscience-other-spine-head-calcium-in-a-ca1-pyramidal-cell-model-154732-model :: modeldb:154732 :: https://modeldb.science/154732

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
