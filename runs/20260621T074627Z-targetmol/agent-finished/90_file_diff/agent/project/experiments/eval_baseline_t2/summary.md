# targetMOL Offline Evaluation

- label: baseline_t2
- tier: 2
- molecules: 3
- ok/failure: 3/0
- proxy score mean/min: 83.8626/83.1176
- official weighted proxy mean/min: 85.0848/84.7907
- elapsed seconds: 47.579

## Failure Summary

- none

## Slowest

- {'target': 'result1.csv', 'row': 1, 'prep_ms': 196, 'vina_ms': 15989, 'smiles': 'O=C(Nc1cc2c(-c3ccc4c(c3)OCO4)c[nH]c2c(Cl)c1F)c1ccc2ccc3ccc4ccccc4c3c2c1'}
- {'target': 'result2.csv', 'row': 1, 'prep_ms': 181, 'vina_ms': 15260, 'smiles': 'COc1ccc(-c2c[nH]c3c(Cl)c(F)c(NC(=O)c4ccc5ccc6ccc7ccccc7c6c5c4)cc23)cc1'}
- {'target': 'result3.csv', 'row': 1, 'prep_ms': 142, 'vina_ms': 14260, 'smiles': 'O=C(Nc1cc(-c2ccc3oc4ccccc4c3c2)nc2cc(F)ccc12)c1ccc2cc(Br)ccc2c1'}
