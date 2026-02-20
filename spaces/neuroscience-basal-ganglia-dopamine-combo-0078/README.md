# COMBO_0078 - Neuroscience Basal Ganglia Dopamine

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
- `neuroscience-other-multiscale-simulation-of-the-striatal-medium-spi-150284-model`: Neuroscience: MultiscaleSimulationOfTheStriatalMediumSpi150284Model
- `neuroscience-other-nacc-medium-spiny-neuron-effects-of-cannabinoid-126640-model`: Neuroscience: NaccMediumSpinyNeuronEffectsOfCannabinoid126640Model
- `neuroscience-other-nigral-dopaminergic-neurons-effects-of-ethanol-o-112359-model`: Neuroscience: NigralDopaminergicNeuronsEffectsOfEthanolO112359Model
- `neuroscience-other-optimal-deep-brain-stimulation-of-the-subthalami-93449-model`: Neuroscience: OptimalDeepBrainStimulationOfTheSubthalami93449Model

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
- neuroscience-other-multiscale-simulation-of-the-striatal-medium-spi-150284-model :: modeldb:150284 :: https://modeldb.science/150284
- neuroscience-other-nacc-medium-spiny-neuron-effects-of-cannabinoid-126640-model :: modeldb:126640 :: https://modeldb.science/126640
- neuroscience-other-nigral-dopaminergic-neurons-effects-of-ethanol-o-112359-model :: modeldb:112359 :: https://modeldb.science/112359
- neuroscience-other-optimal-deep-brain-stimulation-of-the-subthalami-93449-model :: modeldb:93449 :: https://modeldb.science/93449

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
