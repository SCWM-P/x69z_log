# targetMOL Offline Evaluation

- label: final_probe_like_tier2
- tier: 2
- molecules: 3
- ok/failure: 3/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 76.586/72.9841
- official weighted proxy mean/min: 86.7266/84.6084
- elapsed seconds: 17.871

## Failure Summary

- none

## Slowest

- {'target': 'result1.csv', 'row': 1, 'prep_ms': 68, 'vina_ms': 6735, 'smiles': 'O=C(O)c1c(-c2ccc(Cl)cc2)[nH]c2ccc(Oc3ccccc3)cc12'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 107, 'vina_ms': 5678, 'smiles': 'CC(C)(C)NC(=O)c1ccc(Nc2ncc(C#N)cc2F)cn1'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 67, 'vina_ms': 3785, 'smiles': 'CS(=O)(=O)c1ccc(OC2CCN(c3ncccn3)CC2)cc1'}
