# DDI Class-Imbalance Correction (Decagon)

Code for our study evaluating whether SMOTE-style oversampling and class-weighted loss transfer from traditional ML to graph-based drug-drug interaction (DDI) prediction, using Decagon on the SNAP Decagon dataset.

**Paper:** [DOI link here]

## Notebooks

| File | Model condition | Paper section |
|---|---|---|
| `random_forest.ipynb` | Random Forest baseline | 3.2, 4.1 |
| `MLP_(w_&_w_o_SMOTE).ipynb` | MLP, with/without SMOTETomek | 3.2, 3.4, 4.1 |
| `lightgcn.ipynb` | LightGCN | 3.2, 4.1 |
| `decagon_baseline_no_Smote.ipynb` | Decagon, unweighted (hinge loss) | 3.2, 4.1–4.2 |
| `decagon_smote.ipynb` | Decagon + graph augmentation | 3.2, 3.4, 4.4 |
| `decagon_class_weighted.ipynb` | Decagon + weighted BCE | 3.5, 4.2–4.4 |

## Data

[SNAP Decagon dataset](https://snap.stanford.edu/decagon) (Zitnik et al., 2018). Built on the original [Decagon codebase](https://github.com/mims-harvard/decagon), patched for TensorFlow 2 compatibility.

## Notes

Notebooks were run in Google Colab. All models evaluated on the same 25 common + 25 rare side-effect split, 1:1 test sampling.
