# Recipe Recommendation Systems

Two notebooks exploring recipe recommendation from user interactions and recipe features.

## Notebooks

- **[`Homework_RecSys.ipynb`](Homework_RecSys.ipynb)** — EDA and initial experiments with user/item kNN and per-user logistic regression.
- **[`RecSys_FullData.ipynb`](RecSys_FullData.ipynb)** — Extended project on a larger implicit-feedback dataset (up to 5,000 users and 2,000 recipes). Compares popularity, item-KNN, and hybrid **LightFM** using ingredient features and WARP loss.

## Evaluation

Models are compared using Precision@N, Recall@N, and F1@N (plus MAE/RMSE in the homework).
| Model | Precision@5 |
| --- | ---: |
| Popularity | 0.0248 |
| Item-KNN (k=5) | 0.0223 |
| **LightFM** | **0.0273** |
