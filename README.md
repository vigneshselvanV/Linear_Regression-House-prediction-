# Linear Regression

A beginner-friendly **Linear Regression** machine learning project using Python and Scikit-learn.

This project covers the complete basic workflow of building and evaluating a Linear Regression model using a house-price dataset.

## 📌 Topics Covered

- Loading and exploring the dataset
- Checking dataset shape and data types
- Checking missing values
- Separating features and target
- Train-test split
- Building a Linear Regression model
- Training the model
- Understanding coefficients and intercept
- Making predictions
- Comparing actual vs predicted values
- R² Score
- Adjusted R² Score
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Outlier detection using IQR
- Variance Inflation Factor (VIF)

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## 📂 Project Structure

```text
Linear-Regression/
│
├── Linear_regression.ipynb
├── boston_house_prices_clean.csv
└── README.md
```

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Exploration
   ↓
Feature & Target Separation
   ↓
Train-Test Split
   ↓
Linear Regression Model
   ↓
Model Training
   ↓
Prediction
   ↓
Model Evaluation
   ↓
Outlier Analysis
   ↓
VIF Analysis
```

## 📊 Dataset

The project uses a cleaned **Boston House Prices** dataset.

- **Features:** Input variables used to predict house prices
- **Target:** `PRICE`

The target column is separated from the features using:

```python
X = data.drop(columns='PRICE')
y = data['PRICE']
```

## 🤖 Model

The project uses Scikit-learn's `LinearRegression`:

```python
from sklearn.linear_model import LinearRegression

Lin_reg = LinearRegression()
Lin_reg.fit(X_train, y_train)
```

Predictions are then generated using:

```python
y_pred = Lin_reg.predict(X_test)
```

## 📈 Model Evaluation

The following metrics are used to evaluate the model:

### R² Score

Measures how well the model explains the variation in the target variable.

```python
r2_score(y_test, y_pred)
```

### Adjusted R²

Adjusted R² considers the number of features used by the model.

### Mean Squared Error

```python
mse = mean_squared_error(y_test, y_pred)
```

### Root Mean Squared Error

```python
rmse = np.sqrt(mse)
```

## 🔍 Outlier Detection

Outliers are detected using the **IQR (Interquartile Range)** method.

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR
Upper Bound = Q3 + 1.5 × IQR
```

The notebook contains a function to remove outliers from the dataset.

## 📌 VIF Analysis

**Variance Inflation Factor (VIF)** is used to check multicollinearity between features.

A higher VIF indicates that a feature may have a strong relationship with other features.

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Install the required libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 3. Open the notebook

Open:

```text
Linear_regression.ipynb
```

using Jupyter Notebook, JupyterLab, or VS Code.

### 4. Run the cells

Run the notebook cells from top to bottom.

## 🎯 Learning Objective

The main goal of this project is to understand the practical workflow of **Linear Regression**, from preparing the dataset to training, predicting, and evaluating a machine learning model.

---

**Learning ML step by step 🚀**
