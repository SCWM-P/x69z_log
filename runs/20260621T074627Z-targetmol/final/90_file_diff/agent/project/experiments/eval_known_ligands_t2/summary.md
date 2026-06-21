# targetMOL Offline Evaluation

- label: known_ligands_t2
- tier: 2
- molecules: 3
- ok/failure: 0/0
- proxy score mean/min: 72.1679/64.4753
- official weighted proxy mean/min: 80.7067/78.5946
- elapsed seconds: 36.304

## Failure Summary

- result1.csv:1 flags=['rotors_gt_4'] route=[] error=
- result2.csv:1 flags=['tpsa_outside_28_88', 'rotors_gt_4'] route=[] error=
- result3.csv:1 flags=['tpsa_outside_28_88', 'rotors_gt_4'] route=[] error=

## Slowest

- {'target': 'result1.csv', 'row': 1, 'prep_ms': 99, 'vina_ms': 12431, 'smiles': 'Cc1cc(cc(c1Cl)C)OCCCc2c3ccc(cc3[nH]c2C(=O)O)Cl'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 114, 'vina_ms': 12394, 'smiles': 'CNc1c2c(c3cc([nH]c3n1)c4cccc(n4)CNC(=O)COC)n(cn2)C'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 146, 'vina_ms': 9704, 'smiles': 'CC(C)c1nc(on1)N2CCC(CC2)COc3ccc(nc3)c4ccc(cc4)S(=O)(=O)C'}
