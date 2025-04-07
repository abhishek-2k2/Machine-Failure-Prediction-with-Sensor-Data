
# Predictive Maintenance using Machine Learning

## 📌 Project Overview
This project focuses on predicting machine failures based on sensor data in a manufacturing environment using predictive maintenance techniques. By leveraging machine learning algorithms, we aim to reduce downtime, optimize equipment usage, and improve operational efficiency.

---

## 📊 Dataset Information
The dataset used is `predictive_maintenance.csv`, which contains **10,000** observations with the following key features:

- **UDI**: Unique identifier  
- **Product ID**: Categorical product identifier  
- **Type**: Categorical type (L/M/H)  
- **Air temperature [K]**  
- **Process temperature [K]**  
- **Rotational speed [rpm]**  
- **Torque [Nm]**  
- **Tool wear [min]**  
- **Target labels**:  
  - `Machine failure`  
  - `TWF`: Tool Wear Failure  
  - `HDF`: Heat Dissipation Failure  
  - `PWF`: Power Failure  
  - `OSF`: Overstrain Failure  
  - `RNF`: Random Failures  

---

## 🧹 Data Preprocessing

- **Initial Checks**:
  - Verified null values, data types, and duplicates.
  - Ensured unique `Product ID` entries.
  
- **Data Cleaning**:
  - Removed unit brackets from column names for readability.
  - Casted numerical columns to `float64`.
  - Extracted numeric value from `Product ID`.

- **Dropped**:
  - `UDI` and original `Product ID` (used transformed version).

---

## 📈 Exploratory Data Analysis (EDA)

- **Correlation Heatmap** to identify important features.
- **Pairplot & Countplots** to observe class distributions.
- **Failure Type Analysis**:
  - Relationships between sensor features and specific failure types.
  - Class-based behavior visualized for better insight.

---

## 🧠 Model Building

- **Target Variable**: `Machine failure`
- **Type**: Binary classification (0 = No failure, 1 = Failure)

### Models Used:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier

### Workflow:
- Data split using `train_test_split`
- Feature scaling with `StandardScaler`
- Evaluation on test set

---

## 🧪 Model Evaluation

Evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC AUC Score

**Best Performance**:
- Random Forest & XGBoost showed highest accuracy and robustness.

---

## 📦 Libraries Used

```bash
numpy
pandas
matplotlib
seaborn
sklearn
xgboost
```

---

## 🚀 How to Run the Project

1. Clone/download the notebook.
2. Ensure `predictive_maintenance.csv` is in the directory.
3. Install dependencies:
```bash
pip install -r requirements.txt
```
4. Run the notebook:
```bash
jupyter notebook "Major Project.ipynb"
```

---

## 🔭 Future Improvements

- Hyperparameter tuning
- k-fold Cross-validation
- Feature Engineering
- Real-time streaming simulation
- API deployment using Flask or Django
