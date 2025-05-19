## Summary of Analysis

This project involved a thorough Exploratory Data Analysis (EDA) of the Titanic dataset with the following steps:

1. **Data Inspection and Cleaning**  
   - Examined dataset structure and missing values.  
   - Dropped `Cabin` column due to too many missing entries.  
   - Imputed missing `Age` values with the median age.  
   - Filled missing `Embarked` values with the mode (most frequent value).  
   - Encoded categorical variables (`Sex` and `Embarked`) into numeric values.

2. **Exploratory Data Analysis**  
   - Conducted univariate analysis to understand individual feature distributions.  
   - Performed bivariate analysis to study relationships between features and survival.  
   - Created correlation heatmaps and pairplots to explore feature interactions.

3. **Key Findings**  
   - Female passengers had a significantly higher survival rate.  
   - First-class passengers had better survival odds compared to lower classes.  
   - Younger passengers, particularly children, were more likely to survive.  
   - Higher fare was positively correlated with survival, reflecting socio-economic factors.  
   - Due to missing data, `Cabin` was excluded from analysis.

4. **Deliverables**  
   - Cleaned dataset saved as `titanic_cleaned.csv`.  
   - Jupyter Notebook containing all analysis steps and visualizations.  
   - A summary report documenting insights and conclusions.

Through this analysis, we gained practical experience in data cleaning, visualization, and interpreting data patterns to extract meaningful insights.
