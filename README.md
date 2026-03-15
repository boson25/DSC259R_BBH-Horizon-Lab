# DSC259R_BBH-Horizon-Lab
### Predicting Whether a Recipe is Healthy

The goal of this project is to analyze a large recipe dataset and build a predictive model to determine whether a recipe is healthy or unhealthy based on its features.

The project inclued data cleaning, EDA, hypothesis testing, predictive modeling, and fairness analysis. 

---

# Project Website
The full project website is hoted from this repo at: https://boson25.github.io/DSC259R_BBH-Horizon-Lab/#intro

 The website contains our data cleaning and pre-processing, EDA, missingness analysis, hypothesis testing, predictive modeling, fairness analysis, as well as our visualizations and results

 ---

 # Dataset
 The dataset we chose to use was the recipe dataset consisting of attributes for recipes such as cooking time, number of ingredients, nutrition information, recipe tags, and ratings. We avoided using nutrition information attributes in our models to prevent data leakage.

 # Workflow
 1. Data cleaning
    - Remove invalid data
    - Process missing data
    - Generating our "healthiness" variable
2. EDA
   - Univariate distributions
   - Bivariate analysis
   - Aggregations across recipe tags
3. Missingness Question
   - Investigate missing values in the data
   - Conduct permutation test to determine the missingness mechanism
4. Hypothesis testing
   - Permutation test to determine whether short recipes and long recipes differ in average rating. (Null: There is no difference in average rating between short recipes <30 min and long recipes >60 min. Alternative: There is a meaningful difference in average rating between short and long recipes.)
   - Permutation test to determine whether low ingredient recipes and high ingredient recipes differ in average rating. (Null: There is no difference in average rating between low ingredient recipes and high ingredient recipes. Alternative: There is a significant difference in average rating between low ingredient recipes and high ingredient recipes.)
5. Prediction Models
   - Train different models for binary classification of healthiness (if a recipe meets 3 or more of the nutrition conditions we set).
   - Baseline
     - Logistic regression using n_steps, n_ingredients, and log_minutes.
   - Final model
     - Tested logistic regression, random forect, and gradient boosting
     - Gradient boosting performed the best using n_steps_sq to capture non-linear complexity.
6. Fairness Analysis
   - Permutation test to determine if the AUC difference could be due to chance. 
