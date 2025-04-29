# Predicting Happiness Scores: Analyzing Social and Economic Factors

**Contributors**: Emujin Batzorig, Anna Yao, Leah Kim  
**Course**: DS 3021 – Machine Learning Fundamentals  
**Dataset**: [World Happiness Report (2019)](https://www.kaggle.com/datasets/unsdsn/world-happiness)

---

## 🧠 Project Motivation

In this project, we aim to answer:

> **Which factors are the strongest predictors of a country’s happiness score?**  
> Are social and personal factors—such as family support and individual freedom—more predictive of happiness than economic indicators like GDP per capita?

By exploring these questions, we hope to highlight which aspects contribute most significantly to happiness, with potential insights for policymakers, researchers, and other potential users. 

---

## 📊 Dataset Overview

We used the **2019 World Happiness Report**, which contains happiness scores for 155 countries along with:
- **Economic metrics** (e.g., GDP per capita)
- **Social/personal metrics** (e.g., Family, Freedom, Life Expectancy, Generosity, Trust in Government)
- A **Dystopia Residual** score (baseline for comparison)

---

## Methodology

We applied the data science lifecycle:

1. **Data Preprocessing**  
   Selected relevant features, normalized data, and checked for missing values.

2. **Exploratory Data Analysis (EDA)**  
   Visualized relationships between features and the happiness score.

3. **Modeling**  
   - Built a **Linear Regression** model to predict the happiness score.
   - Evaluated performance using **R²** and **Root Mean Squared Error (RMSE)**.
   - Compared feature subsets: Economic-only vs Social-only.
   - Investigated variable importance and ran a feature ablation test (dropping the most important feature).

4. **Evaluation**  
   - Social features: **R² = 0.95**, Economic features: **R² = 0.74**
   - Combined features: **R² = 0.99**, **RMSE = 0.0003**
   - Dropping "Family" reduced R² slightly to **0.971**, RMSE increased to **0.19**

---

## Key Findings

- **Social and personal features** are stronger predictors of happiness than economic ones.
- The **most predictive feature** was **Family**.
- Using **all features** yields the best performance, but the model remains strong even when the top feature is removed.
- Removing "Family", variable with the highest variable importance, brought the RMSE value to 0.19 which is still low. This indicates that our model is rebust and is not reliant on one feature only. 
---

## Future Work

- Use more data from other years (more to observe happiness trends over time.
- Incorporate **causal inference methods** to study directionality.
- Validate model across **regions or income groups**.
- Expand feature set to include **education, mental health, or political stability**.

---

