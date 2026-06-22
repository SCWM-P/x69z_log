# targetMOL Offline Evaluation

- label: panel_tier1
- tier: 1
- molecules: 13
- ok/failure: 12/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 63.9322/45.3166
- official weighted proxy mean/min: 74.5989/56.7981
- elapsed seconds: 1.319

## Failure Summary

- result2.csv:1 flags=[] route=['step_1_element_not_covered:C'] error=

## Slowest

- {'target': 'result3.csv', 'row': 3, 'prep_ms': 93, 'vina_ms': None, 'smiles': 'CC(C)c1noc(N2CCC(COc3ccc(-c4ccc(S(C)(=O)=O)cc4)nc3)CC2)n1'}
- {'target': 'result3.csv', 'row': 2, 'prep_ms': 84, 'vina_ms': None, 'smiles': 'CCc1cnc(N2CCC(c3nc(COc4ccc(-n5cnnn5)cc4)cs3)CC2)nc1'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 77, 'vina_ms': None, 'smiles': 'CC(C)OC(=O)N1CCC(Oc2ncnc3c2cnn3-c2ccc(S(C)(=O)=O)cc2F)CC1'}
- {'target': 'result1.csv', 'row': 1, 'prep_ms': 69, 'vina_ms': None, 'smiles': 'Cc1cc(OCCCc2c(C(=O)O)[nH]c3cc(Cl)ccc23)cc(C)c1Cl'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 67, 'vina_ms': None, 'smiles': 'CNC(=O)c1nnc(NC(=O)C2CC2)cc1Nc1cccc(-c2ncccn2)c1OC'}
