# TargetMOL Research Agent

## Contest Context
- You are working on an AI4S target-molecule task with three injected protein PDB targets.
- Your job is to design target-specific molecules and synthesis routes, then produce one valid submission archive.
- Current public score context: our team is around 0.55+, so structural evidence and target-specific improvement matter more than merely producing a valid package.

## Workspace Contract
- Read target structures from `input_targets/`.
- Write experiments, notes, downloaded metadata, and validation outputs under `experiments/`.
- Write the final submission archive to `candidate/result.zip`.
- Use `.x69z/` through the x69z MCP tools for durable research nodes and decisions.

## Submission Contract
- The final archive must contain exactly `result1.csv`, `result2.csv`, `result3.csv`, and `result.log` in that order.
- Each CSV must have the header `mol_smiles,route`.
- Each CSV should contain one best-supported row unless a local contract explicitly allows more.
- Each route's final product must exactly equal `mol_smiles`.

## Research Expectations
- Identify each target from the PDB sequence or structure before final molecule selection.
- Use target-specific public evidence when available: RCSB, PubChem, ChEMBL, BindingDB, literature, ligand families, and pharmacophore context.
- Use local validation and offline evaluation as reproducible evidence; online docking services such as NVIDIA DiffDock are advisory only.
- Record compact x69z nodes for target analysis, research evidence, candidate design, rejected alternatives, and final validation.

## Done Criteria
Basic requirements, all required:
- `candidate/result.zip` exists and passes zip/CSV parsing.
- Every route final product is checked against `mol_smiles`, using RDKit when possible.
- Local offline evaluation can run on the candidate archive.
- x69z contains durable nodes for target analysis, research evidence, candidate decision, and final validation.

Achievement requirements, at least two required:
- All three targets beat the historical baseline thresholds on offline evaluation: result1 official-weighted proxy 65.1588, result2 65.9992, result3 66.4825.
- All three targets show method-level significant improvement evidence during research, such as a scaffold family, docking pose, pharmacophore, or route strategy that materially improves the evaluated candidate over earlier attempts.
- You can explain why the final result may narrow the gap from our current ~0.55+ competition score toward leading teams, based on target-specific evidence rather than generic molecule guessing.

## Do And Do Not
- Do use memory, x69z nodes, public databases, local scripts, RDKit, offline_eval, and concise citations.
- Do keep API usage low-volume and evidence-driven.
- Do not print or store secrets, API keys, environment dumps, or large raw PDB contents.
- Do not write outside this project workspace except through approved tools.
