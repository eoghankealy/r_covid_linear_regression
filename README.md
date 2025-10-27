# COVID-19 Data Analysis — Linear Regression Project

### Author
**Eoghan Kealy**  
R Programming - Dublin City University project

---

## 📘 Project Overview
This project analyzes COVID-19 data to explore the relationship between **test positivity rates**, **extreme poverty**, and **daily new deaths**.  
A linear regression model with an **interaction term** is used to test whether poverty modifies the effect of test positivity on COVID-19 mortality.

---

## 📊 Data
**File:** `data/nphet_data_merged.csv`  
**Source:** NPET (National Public Health Emergency Team) COVID-19 dataset (merged and cleaned)

**Key Variables**
- `new_deaths` — Daily new reported COVID-19 deaths  
- `positive_rate` — Proportion of tests returning positive  
- `extreme_poverty` — Percentage of the population living in extreme poverty  
- `location` — Country or region identifier  

---

## ⚙️ Methods

1. **Data Cleaning:**  
   Missing values were handled, variable names were standardized, and relevant columns were converted to numeric format for analysis.

2. **Exploratory Analysis:**  
   Summary statistics were produced to understand data distributions, and relationships between key COVID-19 indicators were explored through visualizations.

3. **Linear Regression Model:**  
   A linear regression model was fitted to examine the relationship between COVID-19 deaths and test positivity, including the moderating effect of poverty:
   ```r
   lm(new_deaths ~ positive_rate * extreme_poverty, data = nphet_data_merged)
   ```
   This model tests both the main effects and their interaction to assess whether poverty modifies the association between test positivity and mortality.

4. **Interpretation:**  
   The model output (coefficients and p-values) was interpreted to understand how test positivity and poverty jointly influence COVID-19 mortality rates.



---

## 🧠 Key Findings
- Higher positivity rates are associated with more COVID-19 deaths.  
- The relationship between positivity and deaths becomes stronger in countries with higher extreme poverty.  



---
