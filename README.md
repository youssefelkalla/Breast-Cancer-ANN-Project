# Breast Cancer Diagnosis Using MLP

## Neural Networks Course Project

---

# Project Description

This project implements a Multilayer Perceptron (MLP) neural network for breast cancer diagnosis using tabular medical data.

The model predicts whether the tumor is:

- Malignant (Cancerous)
- Benign (Non-Cancerous)

---

# Dataset

## Dataset Name
Breast Cancer Wisconsin Diagnostic Dataset

## Dataset Link
https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

---

# Tools and Libraries

- Python
- PyTorch
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

# Project Steps

The project includes:

1. Loading the dataset
2. Data preprocessing
3. Feature scaling
4. Splitting the dataset
5. Building the MLP model
6. Training the model
7. Evaluating the model
8. Plotting graphs
9. Performing experiments

---

# Data Preprocessing

The following preprocessing steps were applied:

- Removing unnecessary columns
- Checking missing values
- Encoding labels
- Scaling features using `StandardScaler`
- Splitting data into:
  - Training set
  - Validation set
  - Testing set

---

# MLP Architecture

```text
30 → 32 → 16 → 1
```

The model uses:
- ReLU activation
- Sigmoid output
- Dropout
- Batch Normalization

---

# Training Settings

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | BCELoss |
| Learning Rate | 0.001 |
| Epochs | 100 |

---

# Original Model Results

| Metric | Value |
|---|---|
| Test Accuracy | 95.61% |
| Final Test Loss | 0.2874 |

---

# Experiment 1 — Activation Function

Changed:
```python
ReLU → Tanh
```

## Results

| Activation Function | Accuracy | Loss |
|---|---|---|
| ReLU | 95.61% | 0.2874 |
| Tanh | 98.25% | 0.1395 |

---

# Experiment 2 — Number of Neurons

Changed architecture from:

```text
30 → 32 → 16 → 1
```

to:

```text
30 → 64 → 32 → 1
```

## Results

| Architecture | Accuracy |
|---|---|
| 32 → 16 | 95.61% |
| 64 → 32 | 98.00% |

---

# Experiment 3 — Learning Rate

## Results

| Learning Rate | Accuracy | Loss |
|---|---|---|
| Default LR | 95.61% | 0.2874 |
| Modified LR | 98.25% | 0.1007 |

---

# Visualizations

The project includes:

- Training vs Validation Loss Curve
- Training vs Validation Accuracy Curve
- Confusion Matrix

---

# How To Run The Project

## Step 1
Open the notebook in Google Colab or Jupyter Notebook.

## Step 2
Upload:
```text
data.csv
```

## Step 3
Run all notebook cells.

---

# requirements.txt

```text
torch
pandas
numpy
matplotlib
scikit-learn
```

---

# Repository Structure

```text
Breast-Cancer-MLP-Project/
│
├── Breast_Cancer_MLP_Project.ipynb
├── README.md
├── requirements.txt
│
├── results/
│   ├── loss_curve.png
│   ├── accuracy_curve.png
│   └── experiment_results.png
```

---

# Conclusion

The MLP model achieved high accuracy in breast cancer classification.

Different experiments were performed to study the effect of:
- activation functions
- number of neurons
- learning rate

The experiments showed that tuning the model architecture and hyperparameters improved performance.

---

# Author

Youssef ElKalla
