# Notebooks

This folder contains Jupyter notebooks for exploratory data analysis (EDA) of solar datasets by country.

Each notebook performs:

1. **Data Profiling:** Summary statistics, missing value report.
2. **Outlier Detection & Cleaning:** Handling missing values and flagging outliers.
3. **Exploratory Data Analysis (EDA):**
   - Line plots, scatter plots, and bubble charts
   - Wind rose plots and histograms
   - Correlation heatmaps
4. **Cleaning Impact Analysis:** Comparison of sensor readings pre- and post-cleaning.

**Branching strategy:**
- Each country has its own branch: `eda-<country>` (e.g., `eda-benin`, `eda-togo`).
- Only the respective notebook and relevant scripts are included in each branch.
- `main` contains all notebooks consolidated.
