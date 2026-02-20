# COMBO_0071 - Neuroscience Synaptic Plasticity

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
- `neuroscience-other-oscillating-neurons-in-the-cochlear-nucleus-bahm-87454-model`: Neuroscience: OscillatingNeuronsInTheCochlearNucleusBahm87454Model
- `neuroscience-other-oscillations-phase-of-firing-coding-and-stdp-an-123928-model`: Neuroscience: OscillationsPhaseOfFiringCodingAndStdpAn123928Model
- `neuroscience-other-parametric-computation-and-persistent-gamma-in-a-144579-model`: Neuroscience: ParametricComputationAndPersistentGammaInA144579Model
- `neuroscience-other-prob-inference-of-short-term-synaptic-plasticity-149914-model`: Neuroscience: ProbInferenceOfShortTermSynapticPlasticity149914Model

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
- neuroscience-other-oscillating-neurons-in-the-cochlear-nucleus-bahm-87454-model :: modeldb:87454 :: https://modeldb.science/87454
- neuroscience-other-oscillations-phase-of-firing-coding-and-stdp-an-123928-model :: modeldb:123928 :: https://modeldb.science/123928
- neuroscience-other-parametric-computation-and-persistent-gamma-in-a-144579-model :: modeldb:144579 :: https://modeldb.science/144579
- neuroscience-other-prob-inference-of-short-term-synaptic-plasticity-149914-model :: modeldb:149914 :: https://modeldb.science/149914

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
