# Recipe Recommendation Systems

Two notebooks exploring recipe recommendation from user interactions and recipe features.

## Notebooks

- **[`Homework_RecSys.ipynb`](Homework_RecSys.ipynb)** — EDA and initial experiments with user/item kNN and per-user logistic regression.
- **[`RecSys_FullData.ipynb`](RecSys_FullData.ipynb)** — Extended project on a larger implicit-feedback dataset (up to 5,000 users and 2,000 recipes). Compares popularity, item-KNN, and hybrid **LightFM** using ingredient features and WARP loss.

## Evaluation

Models are compared using Precision@N, Recall@N, and F1@N (plus MAE/RMSE in the homework).
| Model | Precision@5 | Recall@5 | F1@5 |
| --- | --- | --- | ---: |
| Popularity | 0.0248 | **0.0413** | 0.0243 |
| Item-KNN (k=5) | 0.0223 | 0.0321 | 0.0206 |
| LightFM | **0.0273** | 0.0402 | 0.0252 |

## Interpretation

Recipes data could be subject to "popularity bias", meaning there are recipes that are favoured by many (and are probably easy to make). For example, chicken, cupcakes, sandwiches, which everyone likes regardless of personal tastes. This could explain why baseline Popular recommender has relatively high metrics.

Item-based kNN could suffer from the "tunnel vision" problem. Since the model relies heavily on items' ingredients, it tends to recommend dishes that match previous actions. If a person has ingredients in the fridge to make a dish they already cooked, they will probably stick to it, instead of making something new. 

LightFM shows similar results to Popular recommender and with hyperparameter tuning could be better.
