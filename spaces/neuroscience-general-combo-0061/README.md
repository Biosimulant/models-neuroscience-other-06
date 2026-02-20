# COMBO_0061 - Neuroscience General

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
- `neuroscience-other-oscillation-and-coding-in-a-proposed-nn-model-of-123986-model`: Neuroscience: OscillationAndCodingInAProposedNnModelOf123986Model
- `neuroscience-other-oscillations-emerging-from-noise-driven-nns-tchu-168599-model`: Neuroscience: OscillationsEmergingFromNoiseDrivenNnsTchu168599Model
- `neuroscience-other-oversampling-method-to-extract-excitatory-and-in-145803-model`: Neuroscience: OversamplingMethodToExtractExcitatoryAndIn145803Model
- `neuroscience-other-oxytocin-and-vip-involvement-in-prolactin-secret-91893-model`: Neuroscience: OxytocinAndVipInvolvementInProlactinSecret91893Model

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
- neuroscience-other-oscillation-and-coding-in-a-proposed-nn-model-of-123986-model :: modeldb:123986 :: https://modeldb.science/123986
- neuroscience-other-oscillations-emerging-from-noise-driven-nns-tchu-168599-model :: modeldb:168599 :: https://modeldb.science/168599
- neuroscience-other-oversampling-method-to-extract-excitatory-and-in-145803-model :: modeldb:145803 :: https://modeldb.science/145803
- neuroscience-other-oxytocin-and-vip-involvement-in-prolactin-secret-91893-model :: modeldb:91893 :: https://modeldb.science/91893

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
