# COMBO_0063 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-modelling-reduced-excitability-in-aged-ca1-neuro-119266-model`: Neuroscience: ModellingReducedExcitabilityInAgedCa1Neuro119266Model
- `neuroscience-other-modular-grid-cell-responses-as-a-basis-for-hippo-138951-model`: Neuroscience: ModularGridCellResponsesAsABasisForHippo138951Model
- `neuroscience-other-modulation-of-hippocampal-rhythms-by-electric-fi-144589-model`: Neuroscience: ModulationOfHippocampalRhythmsByElectricFi144589Model
- `neuroscience-other-modulation-of-septo-hippocampal-theta-activity-b-116567-model`: Neuroscience: ModulationOfSeptoHippocampalThetaActivityB116567Model

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
- neuroscience-other-modelling-reduced-excitability-in-aged-ca1-neuro-119266-model :: modeldb:119266 :: https://modeldb.science/119266
- neuroscience-other-modular-grid-cell-responses-as-a-basis-for-hippo-138951-model :: modeldb:138951 :: https://modeldb.science/138951
- neuroscience-other-modulation-of-hippocampal-rhythms-by-electric-fi-144589-model :: modeldb:144589 :: https://modeldb.science/144589
- neuroscience-other-modulation-of-septo-hippocampal-theta-activity-b-116567-model :: modeldb:116567 :: https://modeldb.science/116567

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
