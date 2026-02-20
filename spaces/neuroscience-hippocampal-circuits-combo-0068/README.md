# COMBO_0068 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-state-dependent-drug-binding-to-sodium-channels-149174-model`: Neuroscience: StateDependentDrugBindingToSodiumChannels149174Model
- `neuroscience-other-status-epilepticus-alters-dentate-basket-cell-to-155602-model`: Neuroscience: StatusEpilepticusAltersDentateBasketCellTo155602Model
- `neuroscience-other-stochastic-calcium-mechanisms-cause-dendritic-ca-150635-model`: Neuroscience: StochasticCalciumMechanismsCauseDendriticCa150635Model
- `neuroscience-other-theta-phase-precession-in-a-model-ca3-place-cell-98003-model`: Neuroscience: ThetaPhasePrecessionInAModelCa3PlaceCell98003Model

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
- neuroscience-other-state-dependent-drug-binding-to-sodium-channels-149174-model :: modeldb:149174 :: https://modeldb.science/149174
- neuroscience-other-status-epilepticus-alters-dentate-basket-cell-to-155602-model :: modeldb:155602 :: https://modeldb.science/155602
- neuroscience-other-stochastic-calcium-mechanisms-cause-dendritic-ca-150635-model :: modeldb:150635 :: https://modeldb.science/150635
- neuroscience-other-theta-phase-precession-in-a-model-ca3-place-cell-98003-model :: modeldb:98003 :: https://modeldb.science/98003

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
