# CRISP-DM_Modeling_Case

**Case Study - CRISP-DM: Modeling**

1. **Business Understanding**
   1.1 **Objective**
   The goal of this case study is to develop a predictive model for house prices based on the California Housing dataset. The model aims to provide accurate estimates of house prices using demographic and socioeconomic variables derived from the 1990 U.S. census.

2. **Data Understanding**
   2.1 **Data Source**
   The data was obtained from the 1990 U.S. census, with one row per census block group. Each census block group represents the smallest geographical unit for which the U.S. Census Bureau publishes sample data.
   2.2 **Variables**
   The dataset includes variables such as population, average income, average house price, number of rooms in houses, among others. The target variable is the average house price.
   2.3 **Initial Exploration**
   An initial exploratory analysis was conducted to understand the distribution of variables, identify missing values, and analyze correlations between variables.

3. **Data Preparation**
   No cleaning, transformation, or normalization techniques were needed.
   3.3 **Data Splitting**
   A train/test split was performed with 20% of the data allocated for testing.

4. **Modeling**
   4.1 **Model Selection**
   Three modeling techniques were evaluated using MSE (Mean Squared Error) and RMSE (Root Mean Squared Error) as evaluation metrics to penalize large prediction errors.
   a. **Linear Regression**
      - Library: SKLEARN
      - Reference: [SKLEARN Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html#sklearn.linear_model.LinearRegression)
   b. **Support Vector Regression**
      - Library: SKLEARN
      - Reference: [SKLEARN SVR](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVR.html#sklearn.svm.SVR)
   c. **Decision Tree Regression**
      - Library: XGBoost
      - Reference: [XGBoost Decision Tree](https://xgboost.readthedocs.io/en/stable/python/python_api.html)
   Results after training each method are presented below:
  
   | Method                   | MSE             | RMSE            |
   |--------------------------|-----------------|-----------------|
   | Linear Regression        | $55,589.1599    | $235.7735       |
   | Support Vector Regression| $133,201.1542   | $364.9673       |
   | Decision Tree Regression | $22,258.9927    | $149.1945       |

   The Decision Tree Regression method demonstrated the best results and was selected to proceed with the project.

   4.2 **Optimization**
   Hyperparameter optimization was performed using the GridSearchCV method from the SKLEARN library ([SKLEARN GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html#sklearn.model_selection.GridSearchCV)).
   Post-optimization, the model results were as follows:

   | Metrics                 | Before Optimization | After Optimization  | Improvement    |
   |-------------------------|---------------------|---------------------|-----------------|
   | MSE                     | $22,258.9927        | $21,638.1474        | 2.7892%         |
   | RMSE                    | $149.1945           | $147.0991           | 1.4045%         |
"""
