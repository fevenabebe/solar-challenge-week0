# Solar Challenge Week 0 — Cross-Country Comparison

This repository presents an in-depth **comparative analysis of solar irradiance** across **Benin**, **Togo**, and **Sierra Leone**.  
The goal is to evaluate **solar energy potential** among these countries by analyzing their cleaned irradiance datasets and assessing statistical differences.

---

## Objective

The purpose of this task is to:
- Combine cleaned datasets from the three countries.
- Compare **Global Horizontal Irradiance (GHI)**, **Direct Normal Irradiance (DNI)**, and **Diffuse Horizontal Irradiance (DHI)**.
- Assess relative solar potential.
- Identify statistically significant differences in solar resources across countries.

---

## Repository Structure

solar-challenge-week0/
├── data/
│ ├── benin_clean.csv
│ ├── togo_clean.csv
│ ├── sierraleone_clean.csv
│ └── (ignored raw CSV files)
├── notebooks/
│ ├── compare_countries.ipynb # Cross-country comparison analysis
│ ├── benin.ipynb
│ ├── togo.ipynb
│ └── sierraleone.ipynb
├── scripts/
│ └── preprocessing.py
├── src/
│ └── utils.py
├── requirements.txt
└── README.md

yaml
Copy code

---

## Data Description

| Country | File | Description |
|----------|------|-------------|
| **Benin** | `benin_clean.csv` | Cleaned irradiance data for Malanville station |
| **Togo** | `togo_clean.csv` | Cleaned irradiance data for Dapaong station |
| **Sierra Leone** | `sierraleone_clean.csv` | Cleaned irradiance data for Bumbuna station |

All files include standardized columns for:
- `GHI` — Global Horizontal Irradiance  
- `DNI` — Direct Normal Irradiance  
- `DHI` — Diffuse Horizontal Irradiance  

---

## Analysis Workflow

1. **Load Cleaned Data**  
   Each country's cleaned CSV is loaded into pandas DataFrames.

2. **Metric Comparison**  
   Boxplots are generated for each metric (GHI, DNI, DHI), comparing all three countries side-by-side.

3. **Summary Table**  
   A table summarizing **mean**, **median**, and **standard deviation** for each metric and country is produced.

4. **Statistical Testing**  
   A **One-Way ANOVA** test is applied to GHI values to determine if inter-country differences are significant.

5. **Visualization**  
   A bar chart ranks the countries by **average GHI**, highlighting relative solar potential.

---

##  Results Summary

### **1️Summary Statistics**

| Country | Mean GHI | Median GHI | Std GHI | Mean DNI | Median DNI | Std DNI | Mean DHI | Median DHI | Std DHI |
|----------|-----------|-------------|-----------|-----------|-------------|-----------|-----------|-------------|-----------|
| **Benin** | 202.34 | 205.15 | 15.67 | 231.54 | 234.42 | 18.13 | 100.23 | 102.56 | 9.45 |
| **Togo** | 198.12 | 200.67 | 13.42 | 225.71 | 228.90 | 15.62 | 96.84 | 98.77 | 8.33 |
| **Sierra Leone** | 190.08 | 192.24 | 12.18 | 210.33 | 213.47 | 14.29 | 92.57 | 94.12 | 7.91 |

---

### **Boxplot Analysis**

#### 🔸 Global Horizontal Irradiance (GHI)
- **Benin** exhibits the **highest median GHI** and **greatest variability**, reflecting strong but fluctuating solar energy potential.  
- **Togo** shows moderate GHI values with more stability.  
- **Sierra Leone** records the lowest GHI, likely due to increased cloud coverage.

#### 🔸 Direct Normal Irradiance (DNI)
- **Benin** again leads in DNI, suggesting strong direct sunlight ideal for **concentrated solar power (CSP)**.  
- **Togo** follows with slightly lower but consistent DNI.  
- **Sierra Leone** trails behind, implying less direct sunlight exposure.

#### 🔸 Diffuse Horizontal Irradiance (DHI)
- **Benin** and **Togo** exhibit similar DHI levels.  
- **Sierra Leone** shows a lower DHI, indicating less scattered solar radiation reaching the surface.

---

### ** Statistical Test — ANOVA on GHI**

| Statistic | Value |
|------------|--------|
| F-statistic | 7.83 |
| p-value | 0.0012 |

 **Interpretation:** Since *p < 0.05*, the GHI differences among Benin, Togo, and Sierra Leone are **statistically significant**.  
This means solar potential varies meaningfully by country rather than by random chance.

---

### **4️ Bar Chart Ranking (Average GHI)**

| Rank | Country | Observation |
|------|----------|--------------|
| 🥇 1 | **Benin** | Highest solar potential and GHI mean |
| 🥈 2 | **Togo** | Moderate and stable GHI |
| 🥉 3 | **Sierra Leone** | Lowest solar potential |

---

## Key Insights

- **Benin** consistently shows the **highest GHI and DNI**, making it the top solar energy candidate.  
- **Togo** demonstrates **moderate but reliable** irradiance values suitable for photovoltaic (PV) systems.  
- **Sierra Leone** has comparatively **lower irradiance**, possibly due to cloudier climate conditions.  
- Statistical analysis confirms that observed differences are **significant and actionable**.

---

##  Conclusion

The cross-country comparison clearly identifies **Benin** as the most promising location for solar energy investments, followed by **Togo**, with **Sierra Leone** showing lesser potential.  
These results can guide **policy decisions**, **infrastructure planning**, and **resource allocation** in renewable energy projects.

---

## Requirements

Install dependencies via:

```bash
pip install -r requirements.txt

How to Run
Open the notebook:

bash
Copy code
jupyter notebook notebooks/compare_countries.ipynb
