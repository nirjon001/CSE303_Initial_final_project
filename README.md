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

1. Install dependencies: `pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter nbconvert nbclient ipykernel`.
2. Open `Heart_disease_Analysis_Group-7(Updated).ipynb` in Jupyter / VSCode.
3. Make sure `heart_disease_risk_2026.csv` is in the same folder as the notebook.
4. Select the `cse303` kernel and run all cells.

To verify the whole notebook headlessly:

```powershell
python -m jupyter nbconvert --to notebook --execute "Heart_disease_Analysis_Group-7(Updated).ipynb" --output executed.ipynb --ExecutePreprocessor.timeout=600
```

## Disclaimer

The dataset is synthetic (artificially generated). Results reflect this dataset only and
should not be used for real clinical decisions.

## License

MIT License — see [LICENSE](LICENSE).