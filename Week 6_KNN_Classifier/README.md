## KNN Classifier – Learning Overview

This directory contains my learning and experiments related to the K-Nearest Neighbors (KNN) Classifier.

## Concepts Learned

- Understood the working of KNN as a distance-based, lazy learning algorithm

- Learned the difference between KNN classification and KNN regression

- Studied how the choice of K (number of neighbors) affects predictions

Small K → overfitting

Large K → underfitting

- Understood bias–variance tradeoff in the context of KNN

---

## Distance Metrics

- Euclidean distance

- Manhattan distance

- Minkowski distance

- Learned the importance of feature scaling for distance-based models

---

## KNN Hyperparameters

- n_neighbors – number of nearest neighbors

- weights – uniform vs distance-weighted KNN

- metric – distance calculation method

- algorithm – auto, ball_tree, kd_tree, brute

- Learned how these parameters affect model performance and efficiency

---

## Decision Boundary

- Understood the concept of decision boundaries

- Learned why KNN produces non-linear decision boundaries

- Plotted decision boundaries using toy datasets and the Iris dataset

---

## Model Evaluation Metrics

- Accuracy and its limitations on imbalanced datasets

- Confusion Matrix (TP, FP, TN, FN)

- Precision – importance of minimizing false positives

- Recall – importance of minimizing false negatives

- Precision–Recall trade-off

- F1 Score as a balance between precision and recall

---

## Practical Insights

- Understood the role of random_state for reproducibility

- Learned that different random_state values give different but reproducible results

- Studied limitations of KNN:

- Computationally expensive for large datasets

- High memory usage

- Sensitive to noise and feature scaling

---

## Key Takeaways

- KNN is simple, intuitive, and effective for small datasets

- Proper choice of K, distance metric, and scaling is critical

- Accuracy alone is not sufficient for evaluating classification models

- Metric selection should depend on the problem and cost of errors
