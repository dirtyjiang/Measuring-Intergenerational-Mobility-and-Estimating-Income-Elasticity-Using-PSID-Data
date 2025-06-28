This is my first data science project named 'The Matthew Effect in Income: Measuring Intergenerational Mobility and Estimating Income Elasticity Using PSID Data',which is about investigating the intergenerational transmission of income using cleaned and structured data from the Panel Study of Income Dynamics (PSID)

I have excerpted two parts as follows, which can help you quickly understand this project.

## Abstract
This project investigates the intergenerational transmission of income using cleaned and structured data from the Panel Study of Income Dynamics (PSID). The dataset covers three generations of U.S. households and includes information on income, education, gender, and race.

We apply a comprehensive data science workflow, including exploratory data analysis, feature engineering, multiple regression models, and predictive algorithms. The core finding is that the intergenerational income elasticity (IGE) between the second and third generation is approximately **0.33**, indicating a moderate level of income persistence and an income mobility of about **0.67**. This is consistent with the literature on economic inequality in the United States.

Beyond regression, we also test out-of-sample predictive performance using linear models, decision trees, and random forests, both in regression and classification settings. Classification models that segment income into ordinal levels perform slightly better, but the generalization scores across all models remain within a narrow range. This suggests that the explanatory power of the available features may be close to exhaustion.

The project highlights both the **analytical value of intergenerational elasticity estimates** and the **limits of observable features in predicting economic outcomes**. Our findings provide empirical evidence for the persistence of income inequality across generations and shed light on the challenges of achieving upward mobility through observable socioeconomic factors alone.

---
## Project Review

This project utilized a cleaned and curated dataset from **OPENICPSR**, based on the Panel Study of Income Dynamics (PSID), which contains intergenerational information spanning three generations. We conducted a complete data analysis pipeline including exploratory data analysis (EDA), feature engineering, regression modeling, and predictive modeling.

1. **Exploratory Data Analysis**:
   - **Univariate Distribution**: We visualized categorical variables using **pie charts** and continuous variables (e.g., log income) using **kernel density plots** to understand distributional characteristics.
   - **Grouped Variable Interaction**: We employed **violin plots** to explore how third-generation income varies across different subgroups, using parameters like `x` and `hue` to generate layered groupings.

2. **Feature Engineering**:
   - We encoded categorical variables (ordinal and nominal), constructed intergenerational progression features (e.g., education mobility), and computed Pearson correlation matrices with **heatmap visualizations**, laying the foundation for subsequent modeling.

3. **Regression Modeling**:
   - The regression results demonstrated reasonably good behavior. We ultimately estimated the **intergenerational income elasticity (IGE)** for U.S. families to be approximately **0.33**, implying an **income mobility** of about **0.67**.

4. **Predictive Modeling**:
   - Overall generalization performance was not highly satisfactory.
     - In **standard and standardized regression**, we employed linear regression, decision trees, and random forests. The resulting generalized $ R^2 $ values were generally around **0.2**, with minimal variation across models.
     - To address possible feature exhaustion, we transformed the task into a **classification problem** by dividing income into three ordinal classes. Using one-vs-rest logistic regression, multinomial logistic regression, and random forest classifiers, we achieved stable accuracy scores of approximately **0.6**. This indirectly supports the hypothesis of **explanatory power saturation** in the current feature set.
---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🤝 Contributing

Feel free to fork the project, open an issue, or submit a pull request. Let’s collaborate on improving intergenerational mobility analysis!

---
