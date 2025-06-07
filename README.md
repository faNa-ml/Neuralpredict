Here's a professional **README.md** file in **English** for your GitHub project based on the given code:

---

# 🧮 House Price Prediction using Gradient Descent (NumPy + Pandas)

This repository implements a **linear regression model** from scratch using **NumPy** to predict house prices. The model is trained using **batch gradient descent** and visualizes the convergence process over iterations.

---

## 📊 Dataset

The dataset is loaded from an Excel file (`Cleaned_Data.xlsx`) and contains multiple features relevant to housing prices. It assumes:

* `Id` column is dropped as it's not useful for prediction.
* The **last column** is the target: house price.
* All other columns are considered features.

---

## ⚙️ Workflow

### 1. **Preprocessing**

* Data is read using `pandas`.
* Manual standardization (z-score normalization) is applied to both features and target.
* An intercept term (bias) is added as a column of ones.
* Data is randomly split into **80% training** and **20% testing**.

### 2. **Model Training**

* The model uses **gradient descent** to minimize the **Mean Squared Error (MSE)** loss.
* Learning rate: `0.01`
* Epochs: `1000`
* Weights are initialized to zeros.

### 3. **Prediction & Evaluation**

* After training, the model makes predictions on the test set.
* Predicted and true values are **rescaled** back to original units.
* Final **MSE** is printed as the performance metric.

### 4. **Visualization**

* A line plot displays the MSE loss over training epochs.

---

## 📈 Sample Output

```
Epoch 0 - Loss: 1.1035
Epoch 100 - Loss: 0.1712
...
Epoch 900 - Loss: 0.0649

MSE final: 13582.43
```

---

## 🗂️ File Structure

```
├── Cleaned_Data.xlsx       # Input dataset
├── linear_regression.py    # Main Python script
└── README.md               # Documentation
```

---

## ▶️ How to Run

Make sure the required packages are installed:

```bash
pip install pandas numpy matplotlib openpyxl
```

Then run the script:

```bash
python linear_regression.py
```

Ensure the path to `Cleaned_Data.xlsx` is valid or adjust it in the script.

---

## 📌 Notes

* This implementation **does not** use machine learning libraries like Scikit-learn or TensorFlow—everything is implemented from scratch.
* Suitable as an educational example for understanding linear regression and gradient descent.

---


