# Datasets

All nine datasets used in this study are publicly available and can be downloaded
from the UCI Machine Learning Repository or scikit-learn's built-in datasets.

---

## Dataset Sources

| Dataset | Source | Link |
|---|---|---|
| Banknote | UCI ML Repository | [Download](https://archive.ics.uci.edu/ml/datasets/banknote+authentication) |
| Ionosphere | UCI ML Repository | [Download](https://archive.ics.uci.edu/ml/datasets/ionosphere) |
| Sonar | UCI ML Repository | [Download](https://archive.ics.uci.edu/ml/datasets/connectionist+bench+sonar+mines+vs+rocks) |
| Blobs | scikit-learn generated | `sklearn.datasets.make_blobs` |
| Varied | scikit-learn generated | `sklearn.datasets.make_blobs` (varied variance) |
| Wine | UCI ML Repository | [Download](https://archive.ics.uci.edu/ml/datasets/wine) |
| Flame | Available online | [Download](https://cs.joensuu.fi/sipu/datasets/) |
| Glass | UCI ML Repository | [Download](https://archive.ics.uci.edu/ml/datasets/glass+identification) |
| Iris | scikit-learn built-in | `sklearn.datasets.load_iris` |

---

## Dataset Summary

| Dataset | N | Dimensions | Classes | Category |
|---|---|---|---|---|
| Banknote | 1372 | 4 | 2 | Large |
| Ionosphere | 351 | 34 | 2 | Large |
| Sonar | 208 | 60 | 2 | Large |
| Blobs | 1500 | 2 | 3 | Medium |
| Varied | 1500 | 2 | 3 | Medium |
| Wine | 178 | 13 | 3 | Medium |
| Flame | 240 | 2 | 2 | Small |
| Glass | 214 | 9 | 6 | Small |
| Iris | 150 | 4 | 3 | Small |

---

## Usage

Place any downloaded dataset files in this `data/` folder before running
the notebooks. scikit-learn datasets are generated automatically inside
the notebooks and do not require manual download.

> ⚠️ Do not commit any dataset `.csv` files to this repository.
> The `.gitignore` is already configured to exclude them.
