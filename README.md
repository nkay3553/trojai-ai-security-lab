# TrojAI AI Security Lab

An academic Python/Google Colab portfolio exploring model-poisoning metadata,
data integrity, and machine-learning robustness. Developed in connection with
CYBR 422 coursework at the University at Albany.

**Status:** exploratory coursework archive, prepared for portfolio review.
The notebooks contain a mix of metadata analysis, synthetic demonstrations,
and tutorial-based exercises. They are not a validated production detector.

## Included notebooks

| Notebook | Focus | Scope |
| --- | --- | --- |
| [Metadata robustness](notebooks/trojai_robustness.ipynb) | Random Forest, K-Means, feature importance, classification metrics | External TrojAI metadata required |
| [Hash verification](notebooks/r13_hash_verification.ipynb) | SHA-256, Merkle roots, linear regression | Synthetic tampering driven by known labels |
| [Round 7 metaclassifier](notebooks/r7_debackdoor_evaluation.ipynb) | Logistic regression, decision tree, ROC/AUC | Synthetic scores; not measured DeBackdoor results |
| [Robustness tutorial](notebooks/robustness_classification.ipynb) | MNIST color/rotation shifts and time-series regression | Related tutorial with upstream helper code |

## Skills demonstrated

- Python data preparation with pandas and NumPy.
- Supervised learning, clustering, and model evaluation with scikit-learn.
- SHA-256 hashing and Merkle-tree integrity-check logic.
- Visualization and interpretation of model behavior and experimental limitations.

## How to use

1. Open a notebook in Google Colab or Jupyter.
2. For the metadata notebook, supply the appropriate external `METADATA.csv`
   at `/content/sample_data/METADATA.csv`, or update that path in your own copy.
3. For hash verification, supply a Round 13 metadata CSV with `model_name`
   and `poisoned` columns at `sample_data/METADATA (2).csv`.
4. Read [SETUP.md](docs/SETUP.md) for per-notebook prerequisites and
   [LIMITATIONS.md](docs/LIMITATIONS.md) for interpretation of the experiments.

Source notebooks were preserved with added context cells. Saved outputs,
execution counts, and Colab session metadata were removed for publication.
The packaging process checks JSON structure, Python syntax excluding notebook
shell commands, and preservation of original code. It does **not** rerun the
experiments, install historical dependencies, or verify reported metrics.

## Attribution and source materials

- [NIST TrojAI](https://pages.nist.gov/trojai/) provides the project context and
  external benchmark data referenced by the coursework.
- [NIST pruning baseline](https://github.com/usnistgov/trojai-baseline-pruning)
  is referenced by the Round 7 setup cell; its implementation is not included here.
- [AIRi EC23 tutorial](https://github.com/airi-industrial-ai/ec23-tutorial)
  supplies helpers used by the robustness tutorial. That notebook is identified
  as tutorial-based rather than represented as an original algorithm.

The supplied pruning-baseline notebook link could not be retrieved. That
notebook is not included. No benchmark datasets, model weights, upstream
repositories, or source-code PDF screenshots are bundled.

No repository-wide license has been assigned in this preparation step.
Upstream materials retain their own attribution and license requirements.

## Next steps

- Recover the missing pruning-baseline notebook.
- Add appropriately sourced metadata and exact environment information.
- Replace synthetic scores with measured detector outputs for a real evaluation.
- Make random seeds and train/test procedures reproducible.
- Expand the time-series holdout beyond a single observation.
