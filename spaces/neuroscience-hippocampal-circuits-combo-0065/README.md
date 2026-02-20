# COMBO_0065 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-normal-ripples-abnormal-ripples-and-fast-ripples-182134-model`: Neuroscience: NormalRipplesAbnormalRipplesAndFastRipples182134Model
- `neuroscience-other-parvalbumin-positive-basket-cells-differentiate-153280-model`: Neuroscience: ParvalbuminPositiveBasketCellsDifferentiate153280Model
- `neuroscience-other-phase-precession-through-acceleration-of-local-t-143248-model`: Neuroscience: PhasePrecessionThroughAccelerationOfLocalT143248Model
- `neuroscience-other-pinskyrinzelmodel-pinskyrinzelmodel-model`: Neuroscience: PinskyrinzelmodelPinskyrinzelmodelModel

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
- neuroscience-other-normal-ripples-abnormal-ripples-and-fast-ripples-182134-model :: modeldb:182134 :: https://modeldb.science/182134
- neuroscience-other-parvalbumin-positive-basket-cells-differentiate-153280-model :: modeldb:153280 :: https://modeldb.science/153280
- neuroscience-other-phase-precession-through-acceleration-of-local-t-143248-model :: modeldb:143248 :: https://modeldb.science/143248
- neuroscience-other-pinskyrinzelmodel-pinskyrinzelmodel-model :: opensourcebrain:PinskyRinzelModel :: https://github.com/OpenSourceBrain/PinskyRinzelModel

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
