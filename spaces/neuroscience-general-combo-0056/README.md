# COMBO_0056 - Neuroscience General

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
- `neuroscience-other-numerical-integration-of-izhikevich-and-hh-model-117361-model`: Neuroscience: NumericalIntegrationOfIzhikevichAndHhModel117361Model
- `neuroscience-other-nwbshowcase-nwbshowcase-model`: Neuroscience: NwbshowcaseNwbshowcaseModel
- `neuroscience-other-odor-supported-place-cell-model-and-goal-navigat-118434-model`: Neuroscience: OdorSupportedPlaceCellModelAndGoalNavigat118434Model
- `neuroscience-other-olfactory-bulb-granule-cell-effects-of-odor-depr-50210-model`: Neuroscience: OlfactoryBulbGranuleCellEffectsOfOdorDepr50210Model

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
- neuroscience-other-numerical-integration-of-izhikevich-and-hh-model-117361-model :: modeldb:117361 :: https://modeldb.science/117361
- neuroscience-other-nwbshowcase-nwbshowcase-model :: opensourcebrain:NWBShowcase :: https://github.com/OpenSourceBrain/NWBShowcase
- neuroscience-other-odor-supported-place-cell-model-and-goal-navigat-118434-model :: modeldb:118434 :: https://modeldb.science/118434
- neuroscience-other-olfactory-bulb-granule-cell-effects-of-odor-depr-50210-model :: modeldb:50210 :: https://modeldb.science/50210

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
