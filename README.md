# CredAudit: reproduction code

Code for the paper "Auditing the Pipeline, Not the Model: Automated Detection of Leakage and Degenerate Labels in Machine-Learning Credit Scoring" (M. M. Hassan, A. H. M. S. Sadi, M. H. Jamil, A. A. Rian, A. Hossen, M. S. Sayeed), submitted to IEEE Access.

Archived version: https://doi.org/10.5281/zenodo.23323086

## Contents
- `CredAudit_Full_Reproduction.ipynb`: re-runs the whole pipeline, regenerates every table and figure in the paper, and checks each published value against the value it has just computed. It covers:
  - the audit of the three datasets (Section IV),
  - the eight automated checks D1 to D7 and D2b, with their evaluation (Section V),
  - the corrected 13-classifier benchmark, the resampling factorial, calibration and cost-sensitive thresholding (Section VI).

## Data
- DHL-614 (loan prediction): https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset
- GC-1000 (UCI Statlog German Credit): https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data
- LAR-24K (synthetic loan approval): the original Kaggle page is no longer available. The exact file, `loan_data.csv`, is in the Zenodo archive and can be verified with its SHA-256 checksum:
  `f818e574f6a7e4ce3101a5c1ba8ebf404d768d681169e9985b5e45a7565ea97c`

## Environment
Python 3.13.16, scikit-learn 1.6.1, NumPy 2.1.3, pandas 2.2.3, SciPy 1.16.3.
With these versions the pipeline is deterministic, so a re-run reproduces the tables exactly. Model-fitting results can change at the third decimal under other versions.

## How to run
1. Download the datasets and place the files as described at the top of the notebook.
2. Open the notebook (Jupyter or Google Colab) and run all cells in order.

## Licence
MIT (see LICENSE).
