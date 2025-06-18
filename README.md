# 🛒 Retail Sales Predictor

Predict future sales for retail products across different store types using machine learning!  
This project leverages the Big Mart sales dataset to forecast product sales, providing actionable insights for inventory management, marketing, and operational decision-making.

---

## 📌 Project Overview

- **Dataset**: Big Mart sales dataset  
  - 8,523 training records
  - 5,681 test records

- **Goal**: Predict `Item_Outlet_Sales` for various products across multiple stores using both product and outlet characteristics.

- **Model Used**:  
  - XGBoost Regressor (a powerful gradient boosting technique for tabular data)

---

## 🧑‍💻 Features Used

### Product Features
- `Item_Weight`
- `Item_Fat_Content`
- `Item_Visibility`
- `Item_Type`
- `Item_MRP`

### Outlet Features
- `Outlet_Size`
- `Outlet_Location_Type`
- `Outlet_Type`
- `Outlet_Establishment_Year` (engineered into `Outlet_Age`)

_All categorical variables are label encoded. Missing values are handled appropriately._

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Handle missing values (`Item_Weight`, `Outlet_Size`)
- Engineer new feature: `Outlet_Age` (current year - establishment year)
- Remove non-useful identifiers (`Item_Identifier`, `Outlet_Identifier`)
- Label encode all categorical columns

### 2. Model Training
- Model: XGBoost Regressor
- Train-validation split: 75% train, 25% validation
- **Evaluation Metric:** R² Score  
  - Training R² Score: ~0.80  
  - Validation R² Score: ~0.53–0.60 (after feature engineering to reduce overfitting)

### 3. Prediction & Visualization
- Generate predictions for the test dataset
- Visualize:
  - Predicted vs. actual sales on training data
  - Prediction distribution on test data
  - Key insights and trends from model output

---

## 📊 Visualizations

- **Predicted vs Actual Sales**: Assess model fit on training data
- **Test Data Distribution**: Understand the range of predicted sales
- **Feature Impact Graphs**: Insights into important variables

---

## 📁 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

**Main packages:**
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- xgboost

---

## 🚀 Usage

1. **Clone the repository:**
    ```bash
    git clone https://github.com/sahal777/Retail-Sales-Predictor.git
    cd Retail-Sales-Predictor
    ```

2. **Run the notebook:**
    ```bash
    jupyter notebook big_mart.ipynb
    ```

---

## ✍️ Author

**Muhammed Sahal A A**  
[GitHub: sahal777](https://github.com/sahal777)

---

## 📢 Contributions

Feel free to fork, create issues, or submit pull requests!  
For questions or suggestions, open an issue in the repository.

---