# Dataset Information

This directory contains the processed datasets used for the reproduction of the arkSVM paper.

**Dataset Used:** Wisconsin Breast Cancer Dataset (from `sklearn.datasets`).

- **Classes:** 2 (Malignant vs. Benign)
- **Features:** 30 (Numeric, continuous)
- **Modifications:** The features have been Standard Scaled ($Z$-score normalization) so that all SVM distance metrics compute correctly.

The `breast_cancer_processed.npz` file contains the `X_train`, `X_test`, `y_train`, and `y_test` arrays to ensure that all tasks (2.1 through 3.2) operate on the exact same randomized split for perfect reproducibility.
