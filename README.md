# MNIST Digit Classification using PCA and Ridge Regression

This project performs dimensionality reduction on the MNIST dataset using Principal Component Analysis (PCA), followed by binary and multi-class digit classification using Ridge Regression, KNN, LDA, and SVM.

## Dataset

- Dataset: MNIST handwritten digits (28x28 grayscale images)
- Source: [Google Drive – MNIST CSVs](https://drive.google.com/drive/folders/1U7Ng1Kcdd8NucpRS7nTBiaLPa-_CRm9-)
- Each image is reshaped into a 784-dimensional vector.

## Tasks Performed

1. **PCA Analysis**:
   - Reshaped images and applied PCA
   - Visualized the first 16 principal components as digit-like images
   - Determined the number of components (`k = 59`) required to retain **85% of variance**
   - Reconstructed digits using `k` components to validate reconstruction quality

2. **Binary Classification**:
   - Selected digit pairs: (1 vs 8), (3 vs 8), (2 vs 7)
   - Projected data onto first `k` PCs and trained Ridge classifier
   - Achieved accuracies up to **98%**

3. **Multi-Class Classification**:
   - Compared Ridge, KNN, LDA, and SVM on PCA-reduced data
   - **SVM achieved 98.58% test accuracy**

## Results Summary

| Model     | Cross-Validation Accuracy | Test Accuracy |
|-----------|----------------------------|----------------|
| Ridge     | 84.41%                     | 85.61%         |
| KNN       | 97.47%                     | 97.60%         |
| LDA       | 86.51%                     | 87.53%         |
| **SVM**   | **98.43%**                 | **98.58%**     |

## ⚙️ Technologies Used

- Python 3
- scikit-learn
- numpy
- matplotlib
- seaborn

