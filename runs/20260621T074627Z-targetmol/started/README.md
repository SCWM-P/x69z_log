# targetMOL targetmol log checkpoint: started

This checkpoint separates first-class logs from a restorable file snapshot.
The `90_file_diff/` tree preserves original relative paths under `/work/targetmol/run`
for text files selected by suffix.

## Directory guide

- `00_status/`: supervisor state, fatal errors, and remote upload status.
- `01_environment/`: container, network, API, GPU, IO, and filesystem probes.
- `02_baseline/`: v107 baseline generation log.
- `03_agent/llm/`: Codex/LLM conversation JSONL and stderr.
- `03_agent/x69z/`: x69z runtime metadata, PI nodes, and tool usage logs.
- `04_arbitration/`: final baseline/hybrid decision and audit.
- `05_offline_eval/`: local evaluator-proxy summaries for baseline and final outputs.
- `06_targets/`: manifest for raw PDB files copied from `/saisdata` for post-submit study.
- `90_file_diff/`: recursive text-file snapshot preserving original `/work/targetmol/run` relative paths.

## Files copied

- `00_status/status.json`
- `06_targets/README.md`
- `06_targets/manifest.json`
- `90_file_diff/input_targets/README.md`
- `90_file_diff/input_targets/manifest.json`
- `90_file_diff/input_targets/raw/37/target1.pdb`
- `90_file_diff/input_targets/raw/37/target2.pdb`
- `90_file_diff/input_targets/raw/37/target3.pdb`
- `90_file_diff/logs/status.json`
