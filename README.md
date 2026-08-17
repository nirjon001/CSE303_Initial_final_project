<div align="center">

# 🫀 Heart Disease Risk (2026)

### Exploratory Data Analysis & Predictive Modeling

**Statistics for Data Science (CSE303)** · **Group 7**

[![Status: Complete](https://img.shields.io/badge/Status-Complete-2ea44f?style=for-the-badge)](https://github.com/nirjon001/CSE303-Heart-Disease-EDA-Modeling)
[![Python](https://img.shields.io/badge/Python-3.10%20%7C%203.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](Heart_disease_Analysis_Group-7(Updated).ipynb)

</div>

---

A complete data-science project on the **Heart Disease Risk 2026** dataset (Kaggle, synthetic
data by srisyra02): **9000 patients · 27 columns · 0 missing values · 0 duplicates**. The
project walks through the full workflow — describing the data, exploring it from every angle,
and building/comparing predictive models.

> ⭐ This project was completed and received **positive feedback from the instructor**.

---

## 📂 Project Structure

| File | Description |
|:---|:---|
| 📓 `Heart_disease_Analysis_Group-7(Updated).ipynb` | **Main deliverable** — all 8 parts (EDA + predictive modeling), outputs inline |
| 🗄️ `heart_disease_risk_2026.csv` | Dataset (must stay in the same folder as the notebook) |
| 📄 `report.txt` | Text report — Parts 1-7 (exploratory data analysis) |
| 📄 `modeling_report.txt` | Text report — Part 8 (predictive modeling) |
| 📄 `Heart Disease 2026 -Final_Report_Group7.docx` / `.pdf` | Final project report |
| ⚙️ `requirements.txt` | Dependencies (flexible versions, works on any lab PC) |
| 🔒 `requirements-locked.txt` | Exact tested dependency versions |

---

## 🧭 Project Parts

<div align="center">

| # | Part | Focus |
|:-:|:---|:---|
| **1** | Dataset Description | all 27 features (type, meaning, classification) |
| **2** | Central Tendency & Dispersion | mean, median, mode, variance, std, quartiles, IQR |
| **3** | Distribution & Shape | histograms, density + boxplots, skewness, IQR outliers |
| **4** | Categorical Variable Analysis | frequency tables, bar & pie charts |
| **5** | Relationships Between Variables | scatterplots, boxplots, Pearson correlations, 20×20 correlation matrix |
| **6** | Data Quality Assessment | missing values, duplicates, unusual/impossible values |
| **7** | Key Insights | patient risk profile & strongest predictors |
| **8** | Predictive Modeling | Linear (manual normal-equation + sklearn), Logistic, kNN, Decision Tree, Random Forest, Naive Bayes |

</div>

---

## 📊 Key Findings

| Finding | Value |
|:---|:---|
| ⚖️ Class imbalance | 30.3% of patients have heart disease (2727 / 9000) |
| 🎯 Strongest predictors | `max_heart_rate_achieved` (r = **-0.58**), `st_depression` (r = **+0.36**), `age`, `ldl`, `hdl`, `resting_bp_systolic` |
| 🧼 Data quality | completely clean — no preprocessing needed |
| 🧮 Manual linear regression | matches sklearn **exactly** (R² = 0.524, age only) |
| 🏆 Best classifier | **Logistic Regression** — accuracy **0.897**, F1 **0.823**, ROC-AUC **0.950** |

---

## 🚀 Getting Started

### 💻 On your own machine (admin rights)

```bash
pip install -r requirements.txt
jupyter notebook "Heart_disease_Analysis_Group-7(Updated).ipynb"
```

Then select the `cse303` kernel and **Run All**.

> 🔄 Verify the whole notebook headlessly:
>
> ```powershell
> python -m jupyter nbconvert --to notebook --execute "Heart_disease_Analysis_Group-7(Updated).ipynb" --output executed.ipynb --ExecutePreprocessor.timeout=600
> ```

### 🏫 On a lab PC with NO admin rights

The lab machines run **Python 3.10–3.14** with internet access — no admin password needed.

```powershell
python -m pip install --user -r requirements.txt
```

1. Copy the whole folder (notebook + CSV + `requirements.txt`) onto the lab PC.
2. Run the command above — `--user` installs into **your account only**, the lab Python is untouched.
3. In VSCode, select the **system Python** as the kernel:
   - Click the kernel name (top-right of the notebook editor).
   - Choose **"Select Another Kernel"** → **"Python Environments"**.
   - Pick the option labelled like `Python 3.x 64-bit` (`'Python 3.14'`) with a path such as `C:\Users\...\Python\Python3xx`.
   - ⚠️ Do **not** pick any entry that says `venv` / `.venv` (those are empty on the lab PC).
4. Run the notebook (**Run All**).

> 💡 **Notes**
>
> - Older lab Pythons (e.g. 3.10) auto-install slightly older package versions — the notebook only uses basic features.
> - **Fallback:** the notebook already has all plots/outputs saved inline (**0 error cells**), so it displays fully even before you run anything — safe to present.
> - `requirements-locked.txt` holds the exact versions tested, for perfectly reproducible results.

---

## 📦 Tech Stack

<div align="center">

![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![numpy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![matplotlib](https://img.shields.io/badge/matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![seaborn](https://img.shields.io/badge/seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

</div>

---

## ⚠️ Disclaimer

The dataset is **synthetic** (artificially generated). Results reflect this dataset only and
should **not** be used for real clinical decisions.

## 📜 License

Distributed under the **MIT License** — see [`LICENSE`](LICENSE).

---

<div align="center">

**Made with ❤️ for CSE303 · Statistics for Data Science · East West University**

</div>