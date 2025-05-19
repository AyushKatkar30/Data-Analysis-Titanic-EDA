# 🚢 Titanic Dataset - Exploratory Data Analysis (EDA)

## 📊 Objective
To explore and analyze the Titanic dataset to uncover hidden patterns, relationships, and insights about survival using **Python (Pandas, Matplotlib, Seaborn)**.

---

## 📁 Dataset Overview
The dataset used is the classic [Titanic Dataset](https://www.kaggle.com/c/titanic/data), which contains demographic and travel information for passengers aboard the Titanic.

### 🧾 Initial Dataset Info:
- Total Rows: **891**
- Columns: **12**
- Missing Values:
  - `Age`: 177 missing
  - `Cabin`: 687 missing
  - `Embarked`: 2 missing

---

## 🛠️ Data Cleaning
- Dropped `Cabin` column due to excessive missing values.
- Filled missing values:
  - `Age` with median
  - `Embarked` with mode
- Converted categorical columns (`Sex`, `Embarked`) into numerical format using label encoding.
- ✅ Saved the cleaned dataset as `titanic_cleaned.csv`

---

## 🔍 Exploratory Data Analysis (EDA)

### 📌 Univariate Analysis

| Feature    | Chart Used         | Insight |
|------------|--------------------|---------|
| Survived   | `countplot`        | ~60% died, ~40% survived |
| Sex        | `countplot`        | More males than females |
| Pclass     | `countplot`        | Most passengers in 3rd class |
| Age        | `histplot`         | Skewed toward younger adults |
| Fare       | `boxplot`          | Wide fare range with outliers |

---

### 📌 Bivariate Analysis

| Analysis           | Chart Used                  | Observation |
|--------------------|-----------------------------|-------------|
| Survival vs Gender | `countplot(hue='Sex')`      | Females had higher survival |
| Survival vs Pclass | `countplot(hue='Pclass')`   | 1st class survived more |
| Age vs Survival    | `boxplot(x='Survived', y='Age')` | Younger passengers had better chances |
| Fare vs Pclass     | `boxplot(x='Pclass', y='Fare')` | Higher class → Higher fare |

---

### 📌 Correlation Heatmap
```python
plt.figure(figsize=(10,6))
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title("Correlation Heatmap")
