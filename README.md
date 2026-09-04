# VortexTech AI/ML Internship — Week 1: Data Cleaning & EDA

## What this is
A Jupyter notebook (`VortexTech_AI_ML_Week1.ipynb`) that loads the Titanic
dataset (`Titanic-Dataset.csv`), diagnoses data quality issues, cleans them
with documented justification, and produces summary statistics and
visualizations.

## Dataset
`Titanic-Dataset.csv` — 891 passenger records from the Titanic, with columns
for passenger class, name, sex, age, fare, cabin, port of embarkation, and
survival outcome.

## What the notebook does
1. Loads the CSV and inspects it with `.head()` / `.info()`
2. Counts missing values (`isnull().sum()`) and duplicate rows (`duplicated().sum()`)
3. Cleans the data:
   - Fills missing `Age` with the median (robust to outliers)
   - Fills missing `Embarked` with the mode (only 2 missing values)
   - Converts `Cabin` into a `HasCabin` flag instead of imputing, since ~77% of values are missing
   - Converts `Survived`, `Pclass`, `Sex`, and `Embarked` to categorical types
4. Produces summary statistics: `.describe()`, survival value counts, and average fare by passenger class
5. Produces two visualizations: a histogram of passenger age and a bar chart of survival rate by class

## How to run
```bash
pip install pandas matplotlib seaborn jupyter
jupyter notebook VortexTech_AI_ML_Week1.ipynb
```
Run all cells top to bottom. `Titanic-Dataset.csv` must be in the same folder as the notebook.
