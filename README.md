# Support Vector Machine (SVM) Implementation
## Overview
This project explores SVM with sklearn to classify tumors as benign or malignant using the `Breast Cancer Wisconsin Dataset` available in sklearn.
This project focuses on understanding how different SVM kernels behave and how decision boundaries change in a 2D feature space.

## Objectives
1. Visualize the dataset in a 2D feature space.
2. Train SVM classifiers.
3. Visualize the decision boundary.
4. Compare linear, RBF and polynomial kernels.
5. Analyze how kernel choice affects model performance and decision boundaries .

## Dataset
- Name: Breast Cancer Wisconsin 
- Source: sklearn.datasets.load_breast_cancer
- Samples: 569
- Features: 30 numerical features
- Target: 0 (Malignant), 1 (Benign)

## Methodology
1. Load and preprocess the dataset.
2. Select two features for 2D visualization.
3. Train SVM models with different kernels:
    - Linear
    - RBF (Gaussian)
    - Polynomial
4. Plot and compare decision boundaries.
5. Split train-test sets and standardize features.
6. Perform EDA using PCA with two components.
7. Train SVM models (linear,RBF,polynomial) on all features.
8. Compare model behavior and performance.
9. Train a SVM in PCA space and evaluate the model.
10. Visualize decision boundary in PCA space.

## Insights
- SVM trained on full feature space achieved accuracies of 0.95(linear), 0.98(RBF) and 0.87(cubic polynomial), indicating that dataset has subtle non-linear relationships.
- Cubic polynomial kernel is too complex, which reduce s generalization.
- SVM trained on PCA-reduced space achieved 0.99 accuracy, suggesting that PCA captured the most informative variance directions.
- PCA visualization provides interpretability, but using full feature set ensures maximum predictive power.

## Key Takeaways
- Non-linear kernels can capture complex pattern missed by linear models, improving model performance,.
- Overly complex kernels may harm performance due to overfitting.
- Feature standardization is important for SVM, as it relies on distances between points.
- PCA can effectively reduce dimension while maintaining or even improving predictivce power in some cases.

## Why SVM
- Handles high-dimensional data effectively.
- Can model non-linear relationships using kernel functions.
- Margin maximization ensures good generalization and reduces overfitting.

## Tech Stack
- Python
- NumPy
- Scikit-learn
- Matplotlib

## Project Structure
```
├── SVM_Implementation.ipynb
├── README.md
```

## Installation
Clone the repo and install dependencies:

```bash
git clone https://github.com/qianhui-03/Support_Vector_Machine.git
cd Support_Vector_Machine
pip install -r requirements.txt
```

## References
- Scikit-learn. [load_breast_cancer — sklearn.datasets](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
- GeeksforGeeks. [Support Vector Machine Algorithm](https://www.geeksforgeeks.org/machine-learning/support-vector-machine-algorithm/)

