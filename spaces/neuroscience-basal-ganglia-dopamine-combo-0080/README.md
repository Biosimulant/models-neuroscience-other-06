# COMBO_0080 - Neuroscience Basal Ganglia Dopamine

## Scientific Question
How do basal ganglia dopamine mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-rejuvenation-model-of-dopamine-neuron-chan-et-al-97860-model`: Neuroscience: RejuvenationModelOfDopamineNeuronChanEtAl97860Model
- `neuroscience-other-roles-of-subthalamic-nucleus-and-dbs-in-reinforc-97972-model`: Neuroscience: RolesOfSubthalamicNucleusAndDbsInReinforc97972Model
- `neuroscience-other-single-compartment-dorsal-lateral-medium-spiny-n-150556-model`: Neuroscience: SingleCompartmentDorsalLateralMediumSpinyN150556Model
- `neuroscience-other-spiking-neuron-model-of-the-basal-ganglia-humphr-83559-model`: Neuroscience: SpikingNeuronModelOfTheBasalGangliaHumphr83559Model

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
- neuroscience-other-rejuvenation-model-of-dopamine-neuron-chan-et-al-97860-model :: modeldb:97860 :: https://modeldb.science/97860
- neuroscience-other-roles-of-subthalamic-nucleus-and-dbs-in-reinforc-97972-model :: modeldb:97972 :: https://modeldb.science/97972
- neuroscience-other-single-compartment-dorsal-lateral-medium-spiny-n-150556-model :: modeldb:150556 :: https://modeldb.science/150556
- neuroscience-other-spiking-neuron-model-of-the-basal-ganglia-humphr-83559-model :: modeldb:83559 :: https://modeldb.science/83559

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
