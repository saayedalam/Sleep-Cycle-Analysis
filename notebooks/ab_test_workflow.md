## ✅ A/B Testing Workflow (Condensed)

1. **Define Objective**  
   - What are you testing?  
   - Define metric and A/B groups.

2. **Load Data**  
   - Import dataset.  
   - Parse datetime columns if needed.

3. **Clean Data**  
   - Fix missing values, data types, and units (e.g., seconds → hours).  
   - Drop irrelevant or unreliable columns.

4. **Explore Data (EDA)**  
   - Visualize distributions.  
   - Detect outliers and assess group balance.

5. **Define Hypotheses**  
   - H₀: No difference between groups  
   - H₁: There is a difference

6. **Create Groups**  
   - Split data into Group A and Group B based on a chosen feature.

7. **Check Assumptions**  
   - Normality, equal variance, independence.

8. **Run Statistical Test**  
   - Use t-test, Welch’s t-test, or Mann-Whitney U test depending on distribution.

9. **Interpret Results**  
   - Report p-value, significance, and effect size (if applicable).

10. **Visualize Outcome**  
   - Boxplot or barplot comparing groups with clear labels and annotations.

11. **Conclude & Recommend**  
   - Summarize findings, insights, and practical takeaways.