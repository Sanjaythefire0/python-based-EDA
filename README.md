

# 📊 Exploratory Data Analysis (EDA) & Feature Engineering

This repository contains **Exploratory Data Analysis (EDA)** and **Feature Engineering** performed on `Flight Price Prediction` dataset.
The goal is to **clean, transform, and visualize** raw datasets to make them suitable for machine learning models.

---



## ⚙️ Installation & Setup

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/eda-feature-engineering.git
cd eda-feature-engineering
pip install -r requirements.txt
```

Run Jupyter Notebook:

```bash
jupyter notebook notebooks/EDA_FeatureEngineering.ipynb
```

---

## 🛠️ Steps in the Notebook

### 1. Data Loading

* Imported CSV (`pandas.read_csv`) and Excel files (`pandas.read_excel`).
* Handled encoding issues (e.g., `latin-1`).
* Combined multiple datasets (`pd.concat`, `.append`).

### 2. Basic Exploration

* `.head()`, `.info()`, `.describe()`
* Checked column names, datatypes, and dataset shape.

### 3. Handling Missing Values

* Counted missing values (`.isnull().sum()`).
* Visualized with **seaborn heatmap**.
* Filled categorical NaNs with **mode**, numerical with **mean/median**.

### 4. Combining DataFrames

* Used **`pd.merge()`** to add country info to Zomato data.
* Used **`pd.concat()`** to combine train/test datasets.

### 5. Categorical Analysis

* Frequency counts (`.value_counts()`).
* Visualizations:

  * Pie charts (country/city distribution).
  * Countplots (rating colors, online delivery).
  * Barplots (aggregate rating vs. counts).

### 6. Feature Engineering

* **Zomato**: Country merge, city distribution, ratings.
* **Black Friday**:

  * Dropped `User_ID`.
  * Encoded categorical features (`Gender`, `Age`, `City_Category`).
  * Cleaned `Stay_In_Current_City_Years`.
* **Flight Price Prediction**:

  * Extracted day, month, year from `Date_of_Journey`.
  * Extracted hours/minutes from `Arrival_Time` & `Dep_Time`.
  * Mapped `Total_Stops`.
  * Processed `Duration` into numeric hours/minutes.

### 7. Visualization

* **Seaborn & Matplotlib plots**:

  * Distribution plots
  * Correlation heatmap
  * Barplots for categorical features vs target
  * Pie charts for country/city spread

### 8. Preprocessing for ML

* Split train/test using target (`Purchase` presence).
* Train-validation split using `train_test_split`.
* Scaled numerical features using **StandardScaler**.
* Encoded categorical features with **OneHotEncoder / pd.get\_dummies**.


## 🧑‍💻 Tech Stack

* **Python**
* **Pandas, NumPy** – data manipulation
* **Matplotlib, Seaborn** – visualization
* **Scikit-learn** – preprocessing (scaling, encoding, splitting)

