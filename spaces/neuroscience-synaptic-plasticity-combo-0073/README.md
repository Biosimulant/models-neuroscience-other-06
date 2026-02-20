# COMBO_0073 - Neuroscience Synaptic Plasticity

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
- `neuroscience-other-rescue-of-plasticity-by-a-computationally-predic-149162-model`: Neuroscience: RescueOfPlasticityByAComputationallyPredic149162Model
- `neuroscience-other-role-of-active-dendrites-in-rhythmically-firing-83558-model`: Neuroscience: RoleOfActiveDendritesInRhythmicallyFiring83558Model
- `neuroscience-other-roles-of-essential-kinases-in-induction-of-late-149175-model`: Neuroscience: RolesOfEssentialKinasesInInductionOfLate149175Model
- `neuroscience-other-self-influencing-synaptic-plasticity-tamosiunait-87582-model`: Neuroscience: SelfInfluencingSynapticPlasticityTamosiunait87582Model

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
- neuroscience-other-rescue-of-plasticity-by-a-computationally-predic-149162-model :: modeldb:149162 :: https://modeldb.science/149162
- neuroscience-other-role-of-active-dendrites-in-rhythmically-firing-83558-model :: modeldb:83558 :: https://modeldb.science/83558
- neuroscience-other-roles-of-essential-kinases-in-induction-of-late-149175-model :: modeldb:149175 :: https://modeldb.science/149175
- neuroscience-other-self-influencing-synaptic-plasticity-tamosiunait-87582-model :: modeldb:87582 :: https://modeldb.science/87582

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
