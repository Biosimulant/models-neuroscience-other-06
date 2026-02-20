# COMBO_0079 - Neuroscience Basal Ganglia Dopamine

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
- `neuroscience-other-phase-response-curve-of-a-globus-pallidal-neuron-143100-model`: Neuroscience: PhaseResponseCurveOfAGlobusPallidalNeuron143100Model
- `neuroscience-other-rat-subthalamic-projection-neuron-gillies-and-wi-74298-model`: Neuroscience: RatSubthalamicProjectionNeuronGilliesAndWi74298Model
- `neuroscience-other-regulation-of-firing-frequency-in-a-midbrain-dop-127507-model`: Neuroscience: RegulationOfFiringFrequencyInAMidbrainDop127507Model
- `neuroscience-other-regulation-of-the-firing-pattern-in-dopamine-neu-83547-model`: Neuroscience: RegulationOfTheFiringPatternInDopamineNeu83547Model

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
- neuroscience-other-phase-response-curve-of-a-globus-pallidal-neuron-143100-model :: modeldb:143100 :: https://modeldb.science/143100
- neuroscience-other-rat-subthalamic-projection-neuron-gillies-and-wi-74298-model :: modeldb:74298 :: https://modeldb.science/74298
- neuroscience-other-regulation-of-firing-frequency-in-a-midbrain-dop-127507-model :: modeldb:127507 :: https://modeldb.science/127507
- neuroscience-other-regulation-of-the-firing-pattern-in-dopamine-neu-83547-model :: modeldb:83547 :: https://modeldb.science/83547

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
