# Comparative Analysis of Clustering Algorithms: K-Means, DBSCAN, and GMM

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Conference](https://img.shields.io/badge/SRC-Zayed%20University-blue)](https://srcac.zu.ac.ae/2026/)

## 📄 Abstract

This repository contains the implementation of our **SRC (Student Research Conference, Zayed University)** paper on clustering algorithm benchmarking. We present a systematic comparison of three widely used clustering paradigms — **K-Means** (centroid-based), **DBSCAN** (density-based), and **Gaussian Mixture Models (GMM)** (model-based) — across **nine benchmark datasets** with varying sizes, dimensionalities, and cluster complexities.

All algorithms are evaluated under a **unified preprocessing and evaluation pipeline** including duplicate removal, outlier filtering, feature standardization, and PCA-based visualization. Performance is assessed using purity, accuracy, macro-precision, macro-recall, macro F1-score, and silhouette score. Results provide a practical decision-making roadmap for clustering algorithm selection based on empirical data characteristics.

## 📂 Repository Structure

```bash
├── data/
│   └── README.md                    # Dataset descriptions and sources
├── notebooks/
│   ├── kmeans_clustering.ipynb      # K-Means implementation and evaluation
│   ├── dbscan_clustering.ipynb      # DBSCAN implementation and evaluation
│   └── gmm_clustering.ipynb         # GMM implementation and evaluation
├── paper/
│   └── Clustering_Comparative_Analysis.pdf   # Published conference paper
├── LICENSE
├── README.md
└── requirements.txt
```

---

This is the official code for the SRC paper:
**Comparative Analysis of Clustering Algorithms: K-Means, DBSCAN, and Gaussian Mixture Model**
Authors: Peter Yacoub, Mohamed Malek Kaouach, Soud Asaad Soud Alhazba, Mohammad Azmi Al-Betar (Ajman University, UAE)
[Download Paper (PDF)](./paper/Clustering_Comparative_Analysis.pdf)

---

## ⚙️ Methodology

- **Preprocessing:** Duplicate removal, Z-score outlier filtering (|z| > 3), feature standardization
- **Algorithms:** K-Means (RBF), DBSCAN (ε, MinPts tuned via k-distance curve), GMM (EM algorithm)
- **Datasets:** 9 benchmark datasets — Banknote, Ionosphere, Sonar, Blobs, Varied, Wine, Flame, Glass, Iris
- **Evaluation:** Purity, Accuracy, Macro-Precision, Macro-Recall, Macro F1-score, Silhouette Score
- **Visualization:** PCA-based 2D scatter plots for qualitative cluster structure comparison

## 📊 Results Summary

### DBSCAN
| Dataset | Purity | Accuracy | F1 | Silhouette |
|---|---|---|---|---|
| Blobs | 100.00% | 100.00% | 1.000 | 0.81 |
| Flame | 100.00% | 100.00% | 1.000 | 0.31 |
| Wine | 97.46% | 97.46% | 0.977 | 0.63 |
| Iris | 94.90% | 94.90% | 0.943 | 0.67 |

### K-Means
| Dataset | Purity | Accuracy | F1 | Silhouette |
|---|---|---|---|---|
| Varied | 93.10% | 93.10% | 0.929 | 0.63 |
| Wine | 94.00% | 93.80% | 0.933 | 0.28 |
| Flame | 90.90% | 67.30% | 0.772 | 0.40 |

### GMM
| Dataset | Purity | Accuracy | F1 | Silhouette |
|---|---|---|---|---|
| Blobs | 100.00% | 100.00% | 1.000 | 0.81 |
| Varied | 98.87% | 98.87% | 0.989 | 0.60 |
| Ionosphere | 72.57% | 72.57% | 0.621 | 0.22 |

> DBSCAN achieved the strongest overall robustness on non-convex and noisy datasets. K-Means performed best on compact, well-separated clusters. GMM excelled on elliptical and overlapping structures.

## 🗃️ Datasets

Nine labeled benchmark datasets were used for evaluation in a fully unsupervised manner:

| Dataset | N | Dimensions | Classes |
|---|---|---|---|
| Banknote | 1372 | 4 | 2 |
| Ionosphere | 351 | 34 | 2 |
| Sonar | 208 | 60 | 2 |
| Blobs | 1500 | 2 | 3 |
| Varied | 1500 | 2 | 3 |
| Wine | 178 | 13 | 3 |
| Flame | 240 | 2 | 2 |
| Glass | 214 | 9 | 6 |
| Iris | 150 | 4 | 3 |

> ⚠️ Datasets are not included in this repository. See `data/README.md` for download links.

## 🚀 Installation

```bash
git clone https://github.com/Soudk21/clustering-algorithms-benchmark.git
cd clustering-algorithms-benchmark
pip install -r requirements.txt
```

## 📓 Usage

Each notebook is self-contained. Run them independently:

```bash
jupyter notebook notebooks/kmeans_clustering.ipynb
jupyter notebook notebooks/dbscan_clustering.ipynb
jupyter notebook notebooks/gmm_clustering.ipynb
```

## 🤝 Acknowledgments

- Affiliated with: Artificial Intelligence Research Center (AIRC), Ajman University, UAE
- Submitted to: Student Research Conference (SRC), Zayed University

## 📜 Citation

If you use this code or findings in your research, please cite:

```bibtex
@inproceedings{yacoub2025clustering,
title={Comparative Analysis of Clustering Algorithms: K-Means, DBSCAN, and Gaussian Mixture Model},
author={Yacoub, Peter and Kaouach, Mohamed Malek and Alhazba, Soud Asaad Soud and Al-Betar, Mohammad Azmi},
booktitle={Proceedings of the Student Research Conference (SRC), Zayed University},
year={2025}
}
```

## License

MIT License. See [LICENSE](./LICENSE) for details.
