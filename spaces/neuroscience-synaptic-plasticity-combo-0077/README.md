# COMBO_0077 - Neuroscience Synaptic Plasticity

## Scientific Question
How do synaptic changes influence network-level outcomes?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-tag-trigger-consolidation-clopath-and-ziegler-et-118199-model`: Neuroscience: TagTriggerConsolidationClopathAndZieglerEt118199Model
- `neuroscience-other-time-warp-invariant-neuronal-processing-gutig-an-154288-model`: Neuroscience: TimeWarpInvariantNeuronalProcessingGutigAn154288Model
- `neuroscience-other-tonic-clonic-transitions-in-a-seizure-simulation-105507-model`: Neuroscience: TonicClonicTransitionsInASeizureSimulation105507Model
- `neuroscience-other-transmitter-release-and-ca-diffusion-models-yama-120115-model`: Neuroscience: TransmitterReleaseAndCaDiffusionModelsYama120115Model

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
- neuroscience-other-tag-trigger-consolidation-clopath-and-ziegler-et-118199-model :: modeldb:118199 :: https://modeldb.science/118199
- neuroscience-other-time-warp-invariant-neuronal-processing-gutig-an-154288-model :: modeldb:154288 :: https://modeldb.science/154288
- neuroscience-other-tonic-clonic-transitions-in-a-seizure-simulation-105507-model :: modeldb:105507 :: https://modeldb.science/105507
- neuroscience-other-transmitter-release-and-ca-diffusion-models-yama-120115-model :: modeldb:120115 :: https://modeldb.science/120115

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
