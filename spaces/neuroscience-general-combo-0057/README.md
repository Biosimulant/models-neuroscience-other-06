# COMBO_0057 - Neuroscience General

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
- `neuroscience-other-olfactory-bulb-juxtaglomerular-models-carey-et-a-152111-model`: Neuroscience: OlfactoryBulbJuxtaglomerularModelsCareyEtA152111Model
- `neuroscience-other-olfactory-bulb-mitral-and-granule-cell-dendroden-97263-model`: Neuroscience: OlfactoryBulbMitralAndGranuleCellDendroden97263Model
- `neuroscience-other-olfactory-bulb-mitral-cell-gap-junction-nn-model-146030-model`: Neuroscience: OlfactoryBulbMitralCellGapJunctionNnModel146030Model
- `neuroscience-other-olfactory-bulb-network-model-of-gamma-oscillatio-91387-model`: Neuroscience: OlfactoryBulbNetworkModelOfGammaOscillatio91387Model

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
- neuroscience-other-olfactory-bulb-juxtaglomerular-models-carey-et-a-152111-model :: modeldb:152111 :: https://modeldb.science/152111
- neuroscience-other-olfactory-bulb-mitral-and-granule-cell-dendroden-97263-model :: modeldb:97263 :: https://modeldb.science/97263
- neuroscience-other-olfactory-bulb-mitral-cell-gap-junction-nn-model-146030-model :: modeldb:146030 :: https://modeldb.science/146030
- neuroscience-other-olfactory-bulb-network-model-of-gamma-oscillatio-91387-model :: modeldb:91387 :: https://modeldb.science/91387

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
