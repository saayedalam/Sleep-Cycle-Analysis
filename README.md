
# 🌙 A/B Test Project: Weather Data vs. Sleep Quality

This project explores how the presence of weather data affects sleep quality using a real-world sleep tracking dataset. The goal is to determine whether nights with recorded weather conditions (e.g., rain, clear) are associated with better or worse sleep compared to nights labeled as "No weather".

---

## 🎯 Objective

To test whether sleep quality significantly differs between:
- Group A: Nights with `"No weather"`
- Group B: Nights with any known weather type

---

## 📊 Methodology

1. **Data Cleaning & Preparation**
   - Parsed datetime columns
   - Filtered out unreliable entries
   - Focused on relevant variables: `Weather type`, `Sleep Quality`

2. **Group Definition**
   - A = `Weather type == "No weather"`
   - B = `Weather type != "No weather"`

3. **Assumption Checks**
   - Used **Shapiro-Wilk test** to check normality
   - Result: Data **not normally distributed**

4. **Statistical Testing**
   - Used **Mann-Whitney U test** (non-parametric alternative to t-test)
   - Result: **p-value = 0.000** → Statistically significant

5. **Effect Size**
   - Calculated **Cliff’s Delta**: `-0.366`
   - Interpretation: **Medium effect size**

6. **Visualization**
   - Violin plots & overlapping histograms show clear difference in distributions

---

## ✅ Conclusion

There is a **statistically and practically significant difference** in sleep quality between nights with and without recorded weather data. The `"No weather"` group tends to have **lower sleep quality**, possibly due to:
- Environmental disruption
- Incomplete or inconsistent tracking

---

## 📂 Project Structure

```
/data/
   /raw
      sleepcycle_raw.csv
   /processed
      sleepcycle_cleaned.csv
/notebooks/
    02_ab_testing.ipynb.ipynb
README.md
```

---

## 💡 Next Steps

- Explore specific weather types (e.g., Rain vs. Clear)
- Test interactions with temperature or city
- Run additional A/B tests (Steps vs. Sleep Quality, Regularity vs. Sleep Onset)

---

## 🛠️ Tech Stack

- Python, Pandas, Seaborn, Scipy
- Jupyter Notebook
