# COMBO_0058 - Neuroscience General

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
- `neuroscience-other-olfactory-bulb-network-neurogenetic-restructurin-146583-model`: Neuroscience: OlfactoryBulbNetworkNeurogeneticRestructurin146583Model
- `neuroscience-other-olfactory-computations-in-mitral-granule-cell-ci-149415-model`: Neuroscience: OlfactoryComputationsInMitralGranuleCellCi149415Model
- `neuroscience-other-on-stochastic-diff-eq-models-for-ion-channel-noi-128502-model`: Neuroscience: OnStochasticDiffEqModelsForIonChannelNoi128502Model
- `neuroscience-other-optical-stimulation-of-a-channelrhodopsin-2-posi-153196-model`: Neuroscience: OpticalStimulationOfAChannelrhodopsin2Posi153196Model

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
- neuroscience-other-olfactory-bulb-network-neurogenetic-restructurin-146583-model :: modeldb:146583 :: https://modeldb.science/146583
- neuroscience-other-olfactory-computations-in-mitral-granule-cell-ci-149415-model :: modeldb:149415 :: https://modeldb.science/149415
- neuroscience-other-on-stochastic-diff-eq-models-for-ion-channel-noi-128502-model :: modeldb:128502 :: https://modeldb.science/128502
- neuroscience-other-optical-stimulation-of-a-channelrhodopsin-2-posi-153196-model :: modeldb:153196 :: https://modeldb.science/153196

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
