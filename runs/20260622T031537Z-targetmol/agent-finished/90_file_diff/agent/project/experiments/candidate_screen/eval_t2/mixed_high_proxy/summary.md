# targetMOL Offline Evaluation

- label: mixed_high_proxy
- tier: 2
- molecules: 3
- ok/failure: 3/0
- scale note: Local scores are transparent 0-100 proxy/ranking signals using official field names and the semifinal 0.6 molecule / 0.4 synthesis-route top-level weighting; they are not on the hidden leaderboard 0.x scale and should not be subtracted from official scores.
- proxy score mean/min: 77.8016/73.3896
- official weighted proxy mean/min: 86.5946/85.3738
- elapsed seconds: 43.335

## Failure Summary

- none

## Slowest

- {'target': 'result3.csv', 'row': 1, 'prep_ms': 147, 'vina_ms': 17260, 'smiles': 'CC(C)OC(=O)N1CCC(Oc2ncnc3c2cnn3-c2ccc(S(C)(=O)=O)cc2F)CC1'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 92, 'vina_ms': 12300, 'smiles': 'CNC(=O)c1cnc(Nc2ccc(F)cn2)cc1Nc1ccccc1C(N)=O'}
- {'target': 'result1.csv', 'row': 1, 'prep_ms': 113, 'vina_ms': 11584, 'smiles': 'Cc1cc(OCCCc2c(C(=O)O)sc3ccccc23)cc(C)c1Cl'}
