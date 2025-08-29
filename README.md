# 🩺 Week 1 — Disease Prediction Using Patient Data

This project is part of the **DevelopersHub Internship (AI/ML)**.  
The task for **Week 1** was to learn the **basic ML workflow** by predicting heart disease using patient data from the **UCI Cleveland Heart Disease dataset**.

---

## 📂 Project Structure
WEEK1-disease-prediction/
│── data/  
│ └── cleveland.csv # Dataset (renamed from processed.cleveland.data)  
│  
│── notebooks/  
│ ├── 01_load_and_explore.ipynb # Step 1: Load + Explore dataset  
│ ├── 02_preprocessing.ipynb # Step 2: Preprocessing (imputation, scaling, binary target)  
│ ├── 03_eda.ipynb # Step 3: Exploratory Data Analysis  
│ ├── 04_model_training.ipynb # Step 4: Logistic Regression & Random Forest  
│ └── 05_evaluation_report.ipynb # Step 5: One-page summary  
│  
│── week1_report.md # Short 1-page Markdown report  
│── week1_report.pdf # Exported PDF report (submission)  
│── README.md # Project documentation (this file)

---

## 📊 Dataset
- **Source:** UCI Machine Learning Repository (Cleveland subset, processed version)  
- **Size:** 303 rows × 14 columns  
- **Target:** `target` (0–4) → binarized to `target_bin` (0 = healthy, 1 = disease)  

---

## ⚙️ Preprocessing
- **Missing values:**
  - `ca`, `thal` → filled with **mode** (most frequent value)
  - Other numeric columns → filled with **median**
- **Feature scaling:** All features scaled to **[0, 1]** using `MinMaxScaler`
- **Final dataset:** 13 features + 1 binary target (`target_bin`)

---

## 🔍 Exploratory Data Analysis (EDA)
- **Class balance:** ~54% healthy, ~46% disease  
- **Feature distributions:** Plotted histograms for all features  
- **Correlation heatmap:** Studied relationships between features and target

---

## 🤖 Models & Results
Two models were trained and evaluated:

| Model                | Accuracy |
|----------------------|----------|
| Logistic Regression   | **0.8525** |
| Random Forest         | **0.9016** ✅ |

**Selected Model:** Random Forest (better accuracy)

- **Why Random Forest?** Random Forest outperformed Logistic Regression due to its ability to model complex interactions and non-linear relationships among features.

---

## 📄 Outcome
- Learned the complete **ML workflow**:
  - Data loading → preprocessing → EDA → model training → evaluation  
- Produced a **1-page report** (`week1_report.pdf`) for submission  
- **Random Forest** performed better, and it was selected as the **baseline model**.

---


