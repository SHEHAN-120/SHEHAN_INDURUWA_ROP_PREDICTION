# 📌 Rate of Penetration (ROP) Prediction Model

## 🔍 Project Overview

This project focuses on developing a predictive machine learning model for estimating the Rate of Penetration (ROP) in drilling operations. The model predicts ROP using key drilling parameters such as **Weight on Bit (WOB)**, **Rotary Speed (RPM)**, and **Flow Rate**.

A **Savitzky–Golay (SG) filter** was applied to smooth noisy sensor data during preprocessing. This was followed by feature engineering and the implementation of an **XGBoost Regressor** for accurate ROP prediction.

---

## 🛠️ Tech Stack & Tools

* **Language:** Python 3.10
* **IDEs/Editors:** VS Code, Google Colab
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Signal Processing:** SciPy (Savitzky–Golay Filter)
* **Machine Learning:** Scikit-Learn, XGBoost

---

## 📂 Project Structure

* `ROP_Data.ipynb` – Main Jupyter Notebook containing code, analysis, and model training.
* `Data.csv` – Dataset used for model training and testing.
* `rop_prediction_model.pkl` – Saved model file.
* `requirements.txt` – List of dependencies.

---

## 🚀 Installation & Setup

### 1. Prerequisites

Ensure Python 3.10 is installed:

```bash
python --version
```

### 2. Create a Virtual Environment (Windows)

```bash
python -m venv venv
.\venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not available, you can create one with:

```plaintext
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
xgboost
joblib
jupyter
```

---

## 🏃‍♂️ How to Run

### 💻 Option 1: Using VS Code (Recommended)

1. Open the project folder in VS Code.
2. Open `ROP_Data.ipynb`.
3. Select the **venv (Python 3.10) kernel**.
4. Click **Run All**.

---

## 📊 Methodology

* **Data Loading & Cleaning:** Checked for missing values and treated outliers using the **IQR method**.
* **Preprocessing:** Applied **Savitzky–Golay filtering** (Window=7, Polyorder=2) to smooth **RPM, WOB, and Flow**.
* **Feature Engineering:** Created derivative features (e.g., `dRPM`, `dWOB`) and interaction ratios (`RPM_WOB_ratio`).
* **Model Training:** Used **XGBoost Regressor** with `max_depth=2` and `n_estimators=200`.
* **Evaluation:** Evaluated using **R-Squared**, **Adjusted R-Squared**, and **K-Fold Cross Validation**.

---

## 📈 Results

The model outputs the **R-Squared score** and visualizes **Actual vs. Predicted ROP** values to validate performance.


<img width="629" height="548" alt="output" src="https://github.com/user-attachments/assets/b52a5f75-8234-42fc-90eb-bfcfc51a1c1d" />
