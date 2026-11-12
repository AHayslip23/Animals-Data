# Animals Data

A data cleaning, clustering and classification project on a messy wildlife observation dataset (`animal_data_dirty1.csv`). The data covers animal type, country, weight, body length, gender, location coordinates and observation date.

## Repository Contents

| File | Description |
|---|---|
| `Animals Data.ipynb` | Full analysis: cleaning, EDA, k-means clustering and classification models |

## Commit History

### `a9537c1`: Upload of the animals data notebook (2025-12-14)
- **Cleaning:**
  - dropped the animal code and name columns
  - converted observation dates to datetime
  - filled blank countries and other categories with "Unknown"
  - filled missing body length and weight with the column means
  - converted weight from kg to lbs, rounded
  - cleaned up latitude and longitude
  - checked for and removed duplicates
- **EDA:** charts by animal type and country, including a heatmap for Poland.
- **K-means clustering:** grouped the observations into clusters and visualized them.
- **Classification:**
  - **Predicting each observation's cluster:** logistic regression with cross-validation and grid search reached 100% accuracy, which is expected because the clusters were built from the same features.
  - **Predicting whether an animal is male:** logistic regression, grid search, randomized search and a random forest all scored about 48–57%, close to chance.
  - **Feature importance:** plotted the random forest's feature importances, then dropped weight and body length to test a reduced model.

## Tools
Python, pandas, NumPy, scikit-learn, Plotly, matplotlib, seaborn, Jupyter Notebook
