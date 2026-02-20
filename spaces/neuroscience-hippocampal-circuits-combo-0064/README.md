# COMBO_0064 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-multi-comp-ca1-o-lm-interneuron-model-with-varyi-182797-model`: Neuroscience: MultiCompCa1OLmInterneuronModelWithVaryi182797Model
- `neuroscience-other-na-channel-mutations-in-the-dentate-gyrus-thomas-123848-model`: Neuroscience: NaChannelMutationsInTheDentateGyrusThomas123848Model
- `neuroscience-other-network-model-of-the-granular-layer-of-the-cereb-50219-model`: Neuroscience: NetworkModelOfTheGranularLayerOfTheCereb50219Model
- `neuroscience-other-norenbergetal2010-dgbasketcell-norenbergetal2010dgbasketcell-model`: Neuroscience: Norenbergetal2010DgbasketcellNorenbergetal2010dgbasketcellModel

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
- neuroscience-other-multi-comp-ca1-o-lm-interneuron-model-with-varyi-182797-model :: modeldb:182797 :: https://modeldb.science/182797
- neuroscience-other-na-channel-mutations-in-the-dentate-gyrus-thomas-123848-model :: modeldb:123848 :: https://modeldb.science/123848
- neuroscience-other-network-model-of-the-granular-layer-of-the-cereb-50219-model :: modeldb:50219 :: https://modeldb.science/50219
- neuroscience-other-norenbergetal2010-dgbasketcell-norenbergetal2010dgbasketcell-model :: opensourcebrain:NorenbergEtAl2010_DGBasketCell :: https://github.com/OpenSourceBrain/NorenbergEtAl2010_DGBasketCell

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
