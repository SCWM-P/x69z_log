# targetMOL Offline Evaluation

- label: baseline
- tier: 2
- molecules: 3
- ok/failure: 3/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 65.9624/62.8373
- official weighted proxy mean/min: 76.103/74.4616
- elapsed seconds: 13.663

## Failure Summary

- none

## Slowest

- {'target': 'result1.csv', 'row': 1, 'prep_ms': 123, 'vina_ms': 4812, 'smiles': 'O=C(O)c1c(-c2ccc(Cl)cc2)[nH]c2ccc(Oc3ccccc3)cc12'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 89, 'vina_ms': 3756, 'smiles': 'CS(=O)(=O)c1ccc(OC2CCN(c3ncccn3)CC2)cc1'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 49, 'vina_ms': 3717, 'smiles': 'CC(C)(C)NC(=O)c1ccc(Nc2ncc(C#N)cc2F)cn1'}
