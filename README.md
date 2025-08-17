# 🏠 House Price Prediction – Linear Regression from Scratch  

This project implements a **Linear Regression model from scratch** (using only **NumPy, Pandas, and Matplotlib**) to predict house prices on the **Ames Housing Dataset**.  
The notebook demonstrates an end-to-end ML workflow: preprocessing, feature engineering, training, evaluation, and visualization — without using Scikit-learn.  

---

## 📌 Workflow  

### 1. Data Preprocessing  
- Dropped columns with many null values (`PoolQC`, `MiscFeature`, `Alley`, `Fence`, `FireplaceQu`)  
- Filled **numerical features** with mean and **categorical features** with mode  
- Applied **one-hot encoding** on key categorical variables  
- Removed outliers (`GrLivArea > 4000 & SalePrice < 300000`)  
- Split cleaned data back into train & test  

### 2. Feature Engineering  
- Normalized target variable (`SalePrice`) using z-score  
- Dropped `Id` and non-numeric columns  
- Standardized features with training set statistics  
- Added bias term for linear regression  

### 3. Linear Regression Training  
- Implemented:  
  - Cost function (MSE)  
  - Gradient Descent optimization  
- Printed **RMSE** every 100 iterations for training progress  

### 4. Evaluation  
- Inverse-transformed predictions back to original scale  
- Metrics on training data:  
  - **MSE:** 538,432,953.91  
  - **RMSE:** 23,204.16  
  - **MAPE:** 9.18%  
- Top correlated features: `OverallQual`, `GrLivArea`, `TotalBsmtSF`, `GarageCars`, `1stFlrSF`  

### 5. Visualization  
- Scatter plots of top features vs. SalePrice  
- Shows strong linear trends in housing data  

---

## 📊 Results  

✅ Built Linear Regression **without Scikit-learn**  
✅ Achieved **9.18% MAPE** on training data  
✅ Identified **most influential features** affecting house prices  

---

## 🛠️ Tech Stack  
- Python  
- NumPy  
- Pandas  
- Matplotlib  

---

## 🚀 How to Run  

1. Clone the repository  
```bash
git clone https://github.com/yourusername/house-price-prediction.git
cd house-price-prediction
```
2. Install dependencies
pip install numpy pandas matplotlib
Place train.csv and test.csv in the project folder

3. Run the notebook
jupyter notebook HousePricePrediction.ipynb
