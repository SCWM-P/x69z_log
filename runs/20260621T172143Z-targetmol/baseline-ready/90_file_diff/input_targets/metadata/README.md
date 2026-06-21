# Stage-B submit1 recovered targets

Source run: `20260621T074627Z-targetmol`

Competition submission score reported by user:

- `2026-06-21 15:45:05`: `0.531558`
- Previous reference `2026-06-18 20:25:28`: `0.527113`

## Recovered files

- `target1.pdb`
  - source path in evaluator: `/saisdata/37/target1.pdb`
  - sha256 from LogV3 manifest: `5bf7f5f59c497974d761eb8fadbbd6351edadb4fe442a21f3e1470b28c115fe2`
  - chain `J`, residues 171-321, 151 residues
  - no HETATM ligand in mounted PDB
- `target2.pdb`
  - source path in evaluator: `/saisdata/37/target2.pdb`
  - sha256 from LogV3 manifest: `200f137801aebdfeeb49f25895a234eb2913c62d05d84665d96743823dd643bc`
  - chain `A`, residues 580-867, 257 residues
  - no HETATM ligand in mounted PDB
- `target3.pdb`
  - source path in evaluator: `/saisdata/37/target3.pdb`
  - sha256 from LogV3 manifest: `ede6a192bd7661f7c71cdd42ea2f9c6d735674c65a7966603da91e64363b67a1`
  - chain `R`, residues 1-300, 292 residues observed
  - no HETATM ligand in mounted PDB
- `source_manifest.json`
  - copied from LogV3 `06_targets/manifest.json`

No extra `/saisdata` metadata files were present in this submission run.

## Target identity evidence

Agent sequence/metadata research mapped the stripped targets to:

- target1: human MCL1, with representative structures such as RCSB `4HW2`, `4HW3`, `4HW4`, `4ZBF`, `4ZBI`.
- target2: human TYK2 JH2 pseudokinase, with representative structures such as RCSB `3ZON`, `4OLI`, `4WOV`, `5TKD`.
- target3: GPR119, with representative structures such as RCSB `7XZ5`, `7XZ6`, `8VHF`, `8ZR5`, `8ZRK`, `9L79`.

Quick web verification matched the Agent's calls:

- RCSB `4HW2`: MCL-1 inhibitor discovery / fragment-based structure.
- RCSB `4WOV`: TYK2 JH2 pseudokinase ligand-bound structure.
- RCSB `7XZ6`: GPR119-Gs-APD668 complex.

## Submit1 runtime findings

- Run succeeded and final logs uploaded to GitLab/GitHub.
- Baseline implementation: `targetmol_v2`.
- Agent provider: `daseinai`, return code 0, elapsed about `1185s`.
- `x69z_node_limit` was `3`; Agent wrote exactly three durable nodes.
- Arbitration decision: `hybrid`, but accepted replacements were `0` for all targets.
- Final candidate zip was byte-identical to `baseline_result.zip`.
- Final offline Tier 2 proxy inside Agent:
  - target1 affinity `-10.88`, binding_score `80.0`, official proxy `84.7907`
  - target2 affinity `-14.82`, binding_score `80.0`, official proxy `85.0463`
  - target3 affinity `-11.76`, binding_score `80.0`, official proxy `85.4174`
- Official competition score was only `0.531558`, so the local whole-protein Vina/proxy is badly miscalibrated for these stripped target PDBs.

## Submitted baseline molecules

- target1:
  - `O=C(Nc1cc2c(-c3ccc4c(c3)OCO4)c[nH]c2c(Cl)c1F)c1ccc2ccc3ccc4ccccc4c3c2c1`
  - MW about `559.0`, logP about `9.07`, TPSA `63.35`
- target2:
  - `COc1ccc(-c2c[nH]c3c(Cl)c(F)c(NC(=O)c4ccc5ccc6ccc7ccccc7c6c5c4)cc23)cc1`
  - MW about `545.0`, logP about `9.35`, TPSA `54.12`
- target3:
  - `O=C(Nc1cc(-c2ccc3oc4ccccc4c3c2)nc2cc(F)ccc12)c1ccc2cc(Br)ccc2c1`
  - MW about `561.4`, logP about `9.11`, TPSA `55.13`

These are route-valid but medicinal-chemistry poor for the inferred targets: very high logP, polyaromatic, no MCL1 acidic anchor, not TYK2 JH2-like, and not GPR119 agonist-like.

## Immediate specialization direction

1. Stop using the current local Vina score as a primary objective for these stripped targets. It ranked the submitted baseline near `85` official proxy locally while the official score stayed near `0.53`.
2. Build target-specific candidate libraries:
   - MCL1: acidic indole/benzothiophene/tricyclic carboxylate or carboxylic-acid bioisostere motifs for the BH3 groove.
   - TYK2 JH2: imidazopyridazine / pyridazine carboxamide / urea-benzamide allosteric pseudokinase motifs.
   - GPR119: APD668/MBX-2982/GSK-1292263-like lipophilic heteroaryl-piperidine/oxadiazole/sulfonyl agonist motifs.
3. Use local rules for validity/route/SA gates, but use known ligand family similarity and target-specific pharmacophore fit as stronger priors than whole-protein Vina.
4. Use DiffDock selectively for pose sanity on the top few target-specific candidates, not as a bulk scorer.
