# Heart Disease Risk (2026): Exploratory Data Analysis and Predictive Modeling

Course project for **Statistics for Data Science (CSE303)**. A complete analysis of the
Heart Disease Risk 2026 dataset (Kaggle, synthetic data by srisyra02): 9000 patients,
27 columns, no missing values, no duplicates.

## Contents

| File | Description |
|---|---|
| `Heart_disease_Analysis_Group-7(Updated).ipynb` | Main deliverable: all 8 parts (EDA + predictive modeling), with outputs inline |
| `heart_disease_risk_2026.csv` | Dataset (must stay in the same folder as the notebook) |
| `report.txt` | Text report for Parts 1-7 (exploratory data analysis) |
| `modeling_report.txt` | Text report for Part 8 (predictive modeling) |
| `Heart Disease 2026 -Final_Report_Group7.docx` / `.pdf` | Final project report |

## Project parts

1. **Dataset Description** — all 27 features described (type, meaning, classification).
2. **Central Tendency and Dispersion** — mean, median, mode, variance, std, quartiles, IQR.
3. **Distribution and Shape** — histogram + density + boxplot for every numerical feature, skewness and IQR outliers.
4. **Categorical Variable Analysis** — frequency tables, bar and pie charts.
5. **Relationships Between Variables** — scatterplots, boxplots, Pearson correlations, 20x20 correlation matrix.
6. **Data Quality Assessment** — missing values, duplicates, unusual and impossible values.
7. **Key Insights** — patient risk profile and the strongest predictors.
8. **Predictive Modeling** — Linear Regression (manual + sklearn comparison), Logistic Regression, kNN, Decision Tree, Random Forest, Naive Bayes.

## Key findings

- Target is imbalanced: 30.3% of patients have heart disease (2727 of 9000).
- Strongest predictors: `max_heart_rate_achieved` (r = -0.58), `st_depression` (r = +0.36),
  `age`, `ldl`, `hdl`, `resting_bp_systolic`.
- Data is completely clean; no preprocessing needed.
- Logistic Regression is the best classifier (accuracy 0.897, F1 0.823, ROC-AUC 0.950);
  the data is nearly linearly separable, so simpler models win.

## How to run

### On your own machine (with admin rights)

1. Install dependencies: `pip install -r requirements.txt`
2. Open `Heart_disease_Analysis_Group-7(Updated).ipynb` in Jupyter / VSCode.
3. Make sure `heart_disease_risk_2026.csv` is in the same folder as the notebook.
4. Select the `cse303` kernel and run all cells.

To verify the whole notebook headlessly:

```powershell
python -m jupyter nbconvert --to notebook --execute "Heart_disease_Analysis_Group-7(Updated).ipynb" --output executed.ipynb --ExecutePreprocessor.timeout=600
```

### On a lab PC with NO admin rights (Python 3.10-3.14 already installed, internet works)

1. Copy the whole folder (notebook + CSV + requirements.txt) onto the lab PC.
2. Open a terminal and run:

   ```powershell
   python -m pip install --user -r requirements.txt
   ```

   The `--user` flag installs into **your account only** - no admin password needed,
   and the lab Python is never touched.

3. In VSCode pick the **system Python** (the one on `PATH`) as the kernel - not a venv.
4. Run the notebook.

Notes:
- If a lab Python is older (e.g. 3.10), `pip` automatically installs slightly older
  package versions that still work - the notebook only uses basic features.
- **Fallback:** the notebook already has all plots and outputs saved inline (0 error
  cells), so it opens and displays fully even before you run anything - you can always
  present it, and use the terminal only if asked to re-run a cell.
- `requirements-locked.txt` holds the exact versions tested for this project, for
  machines where you want perfectly reproducible results (e.g. your own PC).

## Disclaimer

The dataset is synthetic (artificially generated). Results reflect this dataset only and
should not be used for real clinical decisions.

## License

MIT License — see [LICENSE](LICENSE).