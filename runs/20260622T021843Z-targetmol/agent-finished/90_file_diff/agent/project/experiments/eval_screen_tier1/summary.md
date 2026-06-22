# targetMOL Offline Evaluation

- label: known_ligand_screen_t1
- tier: 1
- molecules: 12
- ok/failure: 11/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 64.5486/57.0253
- official weighted proxy mean/min: 72.6505/69.8421
- elapsed seconds: 2.952

## Failure Summary

- result3.csv:5 flags=['rotors_gt_10'] route=[] error=

## Slowest

- {'target': 'result3.csv', 'row': 5, 'prep_ms': 408, 'vina_ms': None, 'smiles': 'CCCCCCCC/C=C/CCCCCCCC(=O)OC[C@@H](O)CO[P@](=O)(O)OCC[N+](C)(C)C'}
- {'target': 'result3.csv', 'row': 4, 'prep_ms': 200, 'vina_ms': None, 'smiles': 'CC[C@@H](Oc1ccc(C(=O)C2CC2)cc1)c1nc(-c2ccc(C(=O)N[C@H](C)CO)c(F)c2)no1'}
- {'target': 'result3.csv', 'row': 2, 'prep_ms': 178, 'vina_ms': None, 'smiles': 'CCc1cnc(N2CCC(c3nc(COc4ccc(-n5cnnn5)cc4)cs3)CC2)nc1'}
- {'target': 'result1.csv', 'row': 1, 'prep_ms': 169, 'vina_ms': None, 'smiles': 'O=C(O)c1c(CCCOc2cccc3ccccc23)c2cccc3c2n1CCCS3=O'}
- {'target': 'result3.csv', 'row': 3, 'prep_ms': 169, 'vina_ms': None, 'smiles': 'CC(C)c1noc(N2CCC(COc3ccc(-c4ccc(S(C)(=O)=O)cc4)nc3)CC2)n1'}
