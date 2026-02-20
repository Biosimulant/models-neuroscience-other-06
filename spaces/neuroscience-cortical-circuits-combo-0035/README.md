# COMBO_0035 - Neuroscience Cortical Circuits

## Scientific Question
How do cortical circuit motifs transform and propagate activity?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-towards-a-virtual-c-elegans-palyanov-et-al-2012-147938-model`: Neuroscience: TowardsAVirtualCElegansPalyanovEtAl2012147938Model
- `neuroscience-other-turtle-visual-cortex-model-nenadic-et-al-2003-wa-94845-model`: Neuroscience: TurtleVisualCortexModelNenadicEtAl2003Wa94845Model
- `neuroscience-other-updated-tritonia-swim-cpg-calin-jagemann-et-al-2-93325-model`: Neuroscience: UpdatedTritoniaSwimCpgCalinJagemannEtAl293325Model

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
- neuroscience-other-towards-a-virtual-c-elegans-palyanov-et-al-2012-147938-model :: modeldb:147938 :: https://modeldb.science/147938
- neuroscience-other-turtle-visual-cortex-model-nenadic-et-al-2003-wa-94845-model :: modeldb:94845 :: https://modeldb.science/94845
- neuroscience-other-updated-tritonia-swim-cpg-calin-jagemann-et-al-2-93325-model :: modeldb:93325 :: https://modeldb.science/93325

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
