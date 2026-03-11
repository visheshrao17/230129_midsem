# Data Directory

## Dataset Source

This project uses the **Iris dataset** from scikit-learn (`sklearn.datasets.load_iris`).

- **Samples:** 150
- **Features:** 4 (sepal length, sepal width, petal length, petal width)
- **Classes:** 3 (Setosa, Versicolour, Virginica)
- **Task:** Multi-class classification (binary subsets used for SVM experiments)

## Why Iris?

- Well-understood benchmark dataset suitable for kernel method experiments
- Contains sufficient samples (150) for meaningful train/test splits
- Multiple features allow exploration of kernel behavior
- Non-linearly separable classes (Versicolour vs Virginica) are ideal for SVM experiments

## Preprocessing Steps

1. **Feature Selection:** All 4 features are used
2. **Normalization:** StandardScaler (zero mean, unit variance) applied to all features
3. **Binary Classification:** For SVM experiments, classes 1 and 2 (Versicolour and Virginica) are selected to create a binary classification problem
4. **Train/Test Split:** 80/20 stratified split with `random_state=42` for reproducibility

## Additional Datasets

For some experiments, `sklearn.datasets.make_classification` is also used to generate synthetic data with controlled properties (e.g., varying noise levels for failure case analysis).

## Notes

- No external data files need to be downloaded
- All datasets are loaded programmatically via scikit-learn
- Raw data is not stored in this directory to avoid redundancy
