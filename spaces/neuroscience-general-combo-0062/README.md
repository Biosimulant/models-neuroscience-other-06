# COMBO_0062 - Neuroscience General

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
- `neuroscience-other-paired-turbulence-and-light-effect-on-calcium-in-53427-model`: Neuroscience: PairedTurbulenceAndLightEffectOnCalciumIn53427Model
- `neuroscience-other-paradoxical-gaba-mediated-excitation-lewin-et-al-146504-model`: Neuroscience: ParadoxicalGabaMediatedExcitationLewinEtAl146504Model
- `neuroscience-other-parallel-network-simulations-with-neuron-miglior-64229-model`: Neuroscience: ParallelNetworkSimulationsWithNeuronMiglior64229Model
- `neuroscience-other-perturbation-sensitivity-implies-high-noise-and-144027-model`: Neuroscience: PerturbationSensitivityImpliesHighNoiseAnd144027Model

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
- neuroscience-other-paired-turbulence-and-light-effect-on-calcium-in-53427-model :: modeldb:53427 :: https://modeldb.science/53427
- neuroscience-other-paradoxical-gaba-mediated-excitation-lewin-et-al-146504-model :: modeldb:146504 :: https://modeldb.science/146504
- neuroscience-other-parallel-network-simulations-with-neuron-miglior-64229-model :: modeldb:64229 :: https://modeldb.science/64229
- neuroscience-other-perturbation-sensitivity-implies-high-noise-and-144027-model :: modeldb:144027 :: https://modeldb.science/144027

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
