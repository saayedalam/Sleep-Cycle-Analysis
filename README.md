# 🌙 A/B Test Project: Weather Data vs. Sleep Quality

This project explores how the presence of weather data affects sleep quality using a real-world sleep tracking dataset. The goal is to determine whether nights with recorded weather conditions (e.g., rain, clear) are associated with better or worse sleep compared to nights labeled as "No weather".

---

## 🎯 Objective

To test whether sleep quality significantly differs between:

- **Group A**: Nights with "No weather"
- **Group B**: Nights with any known weather type

---

## 📊 Methodology

### 1. Data Cleaning & Preparation
- Parsed datetime columns
- Filtered out unreliable entries
- Focused on relevant variables: `Weather type`, `Sleep Quality`

### 2. Group Definition
- A = `Weather type == "No weather"`
- B = `Weather type != "No weather"`

### 3. Assumption Checks
- Used **Shapiro-Wilk test** to check normality
- ❌ Result: Data **not normally distributed**

### 4. Statistical Testing
- Used **Mann-Whitney U test** (non-parametric alternative to t-test)
- ✅ Result: **p-value = 0.000** → Statistically significant

### 5. Effect Size
- Calculated **Cliff’s Delta**: `-0.366`
- 📐 Interpretation: **Medium effect size**

### 6. Practical Impact
- Compared **mean** and **median** values:
  - Mean sleep quality increased from **0.761 → 0.855** (+12.4%)
  - Median increased from **0.790 → 0.880** (+11.4%)
- The increase in both mean and median confirms that the difference is **practically meaningful**, not just statistical.

### 7. Visualization
- Violin plots and overlapping histograms show clear distribution differences

---

## 🔍 Deep Dive: Fog vs. Rainy Showers

To identify which specific weather types may influence sleep the most, we compared **Fog** (high, consistent sleep quality) and **Rainy Showers** (lower and more variable).

**Results:**
- Mean sleep quality:
  - Fog: **0.895**
  - Rainy Showers: **0.883**
- Median sleep quality:
  - Fog: **0.930**
  - Rainy Showers: **0.840**
- Mann-Whitney U test p-value: **0.795** → ❌ Not statistically significant
- Cliff’s Delta: **0.167** → ✅ Small effect size

While **Fog** showed slightly higher sleep quality, the difference was not statistically significant. This suggests a minor trend in favor of Fog, but not strong enough to draw firm conclusions.

---

## ✅ Conclusion

There is a statistically and practically significant difference in sleep quality between nights with and without recorded weather data. The "No weather" group tends to have lower sleep quality, possibly due to:

- 🌧️ Environmental disruption
- 📉 Incomplete or inconsistent tracking

This insight may help inform how data quality and weather influence personal sleep tracking or wellness decisions.

---

## 📂 Project Structure

```
/data/
    /raw
        sleepcycle_raw.csv
    /processed
        sleepcycle_cleaned.csv
/notebooks/
    02_ab_testing.ipynb
README.md
```

---

## 💡 Next Steps

- Explore specific weather types (e.g., Rain vs. Clear)
- Test interactions with temperature or city
- Run additional A/B tests (e.g., Steps vs. Sleep Quality, Regularity vs. Sleep Onset)

---

## 🛠️ Tech Stack

Python, Pandas, NumPy, SciPy, Seaborn, Matplotlib, Jupyter Notebook, Git, GitHub
