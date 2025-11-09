# ┌─────────────────────────────────────────────
# │ Solar Challenge Week 0
# └─────────────────────────────────────────────

This repository contains exploratory data analysis (EDA), data cleaning scripts, and visualizations for solar datasets of multiple countries. The goal is to profile, clean, and analyze each country’s solar dataset to prepare it for comparison and region-ranking tasks.

---

# ┌─────────────────────────────────────────────
# │ Repository Structure
# └─────────────────────────────────────────────

```
solar-challenge-week0/
├── data/               # Contains raw and cleaned CSV files (ignored in git)
├── notebooks/          # Jupyter notebooks for EDA per country
│   ├── benin.ipynb
│   ├── togo.ipynb
│   ├── sierraleone.ipynb
│   └── data/           # Optional notebook-specific data (ignored)
├── scripts/            # Python scripts for data cleaning or preprocessing
├── src/                # Source code for analysis or reusable modules
├── tests/              # Unit tests for scripts or modules
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

# ┌─────────────────────────────────────────────
# │ Data
# └─────────────────────────────────────────────

- All raw datasets are located in `data/` (e.g., `benin-malanville.csv`, `togo-dapaong_qc.csv`, `sierraleone-bumbuna.csv`).  
- Cleaned datasets are also saved here (e.g., `benin_clean.csv`, `togo_clean.csv`).  
- **Important:** The `data/` folder is added to `.gitignore` to avoid committing large CSVs.

---

# ┌─────────────────────────────────────────────
# │ Branches
# └─────────────────────────────────────────────

- `main` — Contains all notebooks and scripts consolidated.  
- `setup-task` — Only the default notebook for setup instructions.  
- `eda-<country>` — One branch per country containing only that country’s notebook and relevant scripts.  
  - Example: `eda-benin` contains `benin.ipynb` only.  
  - Example: `eda-togo` contains `togo.ipynb` only.  

---

# ┌─────────────────────────────────────────────
# │ Notebooks
# └─────────────────────────────────────────────

Each notebook performs:

1. Data profiling (summary statistics, missing values, etc.)  
2. Outlier detection and cleaning  
3. Exploratory Data Analysis (EDA)  
   - Line plots, scatter plots, bubble charts  
   - Wind rose plots and histograms  
   - Correlation heatmaps  
4. Cleaning impact comparison (pre/post-clean)  

---

# ┌─────────────────────────────────────────────
# │ Requirements
# └─────────────────────────────────────────────

Install dependencies via pip:

```bash
pip install -r requirements.txt
```

Dependencies include:

- `pandas`, `numpy` — data handling  
- `matplotlib`, `seaborn` — visualization  
- `scipy` — statistical analysis  

---

# ┌─────────────────────────────────────────────
# │ How to Run
# └─────────────────────────────────────────────

1. Clone the repository:

```bash
git clone https://github.com/fevenabebe/solar-challenge-week0.git
cd solar-challenge-week0
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Open and run notebooks:

```bash
jupyter notebook notebooks/benin.ipynb
```

- Replace `benin.ipynb` with any other country notebook.

---

# ┌─────────────────────────────────────────────
# │ Notes
# └─────────────────────────────────────────────

- The repository is designed to **keep country analyses isolated** in their branches.  
- `main` contains **all notebooks and scripts** for a global overview.  
- Do not commit CSV files — keep all large datasets local in `data/`.  

---

# ┌─────────────────────────────────────────────
# │ References
# └─────────────────────────────────────────────

- Solar irradiance datasets per country  
- EDA and data cleaning techniques in Python  
- Visualization best practices (matplotlib, seaborn)
