# targetMOL Offline Evaluation

- label: baseline
- tier: 2
- molecules: 3
- ok/failure: 3/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 66.2544/63.1181
- official weighted proxy mean/min: 76.395/74.7424
- elapsed seconds: 12.466

## Failure Summary

- none

## Slowest

- {'target': 'result1.csv', 'row': 1, 'prep_ms': 176, 'vina_ms': 4420, 'smiles': 'O=C(O)c1c(-c2ccc(Cl)cc2)[nH]c2ccc(Oc3ccccc3)cc12'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 47, 'vina_ms': 3573, 'smiles': 'CC(C)(C)NC(=O)c1ccc(Nc2ncc(C#N)cc2F)cn1'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 51, 'vina_ms': 3170, 'smiles': 'CS(=O)(=O)c1ccc(OC2CCN(c3ncccn3)CC2)cc1'}
