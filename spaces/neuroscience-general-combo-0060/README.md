# COMBO_0060 - Neuroscience General

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
- `neuroscience-other-osb-metadata-osbmetadata-model`: Neuroscience: OsbMetadataOsbmetadataModel
- `neuroscience-other-osb-model-validation-osbmodelvalidation-model`: Neuroscience: OsbModelValidationOsbmodelvalidationModel
- `neuroscience-other-osb-status-osbstatus-model`: Neuroscience: OsbStatusOsbstatusModel
- `neuroscience-other-osb-videos-osbvideos-model`: Neuroscience: OsbVideosOsbvideosModel

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
- neuroscience-other-osb-metadata-osbmetadata-model :: opensourcebrain:OSB_Metadata :: https://github.com/OpenSourceBrain/OSB_Metadata
- neuroscience-other-osb-model-validation-osbmodelvalidation-model :: opensourcebrain:osb-model-validation :: https://github.com/OpenSourceBrain/osb-model-validation
- neuroscience-other-osb-status-osbstatus-model :: opensourcebrain:OSB_Status :: https://github.com/OpenSourceBrain/OSB_Status
- neuroscience-other-osb-videos-osbvideos-model :: opensourcebrain:OSB_Videos :: https://github.com/OpenSourceBrain/OSB_Videos

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
