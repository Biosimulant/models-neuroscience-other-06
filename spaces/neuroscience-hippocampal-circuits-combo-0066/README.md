# COMBO_0066 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-poirazi2003-ca1pyramidalcell-poirazi2003ca1pyramidalcell-model`: Neuroscience: Poirazi2003Ca1pyramidalcellPoirazi2003ca1pyramidalcellModel
- `neuroscience-other-role-for-short-term-plasticity-and-olm-cells-in-168314-model`: Neuroscience: RoleForShortTermPlasticityAndOlmCellsIn168314Model
- `neuroscience-other-roles-of-i-a-and-morphology-in-ap-prop-in-ca1-py-118014-model`: Neuroscience: RolesOfIAAndMorphologyInApPropInCa1Py118014Model
- `neuroscience-other-shaping-of-action-potentials-by-different-types-140471-model`: Neuroscience: ShapingOfActionPotentialsByDifferentTypes140471Model

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
- neuroscience-other-poirazi2003-ca1pyramidalcell-poirazi2003ca1pyramidalcell-model :: opensourcebrain:Poirazi2003-CA1PyramidalCell :: https://github.com/OpenSourceBrain/Poirazi2003-CA1PyramidalCell
- neuroscience-other-role-for-short-term-plasticity-and-olm-cells-in-168314-model :: modeldb:168314 :: https://modeldb.science/168314
- neuroscience-other-roles-of-i-a-and-morphology-in-ap-prop-in-ca1-py-118014-model :: modeldb:118014 :: https://modeldb.science/118014
- neuroscience-other-shaping-of-action-potentials-by-different-types-140471-model :: modeldb:140471 :: https://modeldb.science/140471

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
