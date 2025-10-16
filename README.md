# Practical Lab 2: Multivariate Linear Regression, Non-Parametric Models and Cross-Validation

##  Project Members:
    1. Jarius Bedward #8841640

## Project Summary:

This project analyzes the Scikit-Learn diabetes dataset to predict the progression of diabetes one year after baseline. To do this univariate and
multivariate polynomial regression, decsion trees, k-nearest Neighbors (kNN), and Logistic Regression is used. The models aim to help physicians identify patients at risk.
The project focuses on evaluating model performance using R-squared, Mean Absolute Error(MAE), and Mean Absolute Percentage Error(MAPE)

**Key Features:**
- **Data Preprocessing:**
  - Load diabetes dataset using sklearn built in data set
  - Explore and clean the data(check forf missing values)
  - Split dataset into train (75%), validation (10%), and test (15%) sets
- **Exploratory Data Analysis:**
  - Summary statistics, histograms, scatter plots, and correlation matrix
  - Insights about feature distributions and potential relationships with the target variable
- **Univariate Polynomial Regression**
  - Fit polynomial models on BMI feature for degrees 0-5
  - Evaluate Models on training, validation and test sets using R2, MAE and MAPE
  - Plot train, validation, test data along with polynomial fit
  - Predict disease progression for chosen BMI values
  - Calculate number of trainable parameters
- **Multivariate Polynomial Regression, Decision Trees, kNN, Logistic Regression:**
  - Use all features for multivariate models
  - Fit two models per type
  - Compare models for selection
- **Visualization:**
  - Scatter plots and regression curves for univariate BMI models
  - Visual summaries for train, validation and test sets
  - 

## Requirements:
    - pip install -r requirements.txt

##  🎯  How to Run:

1. Clone this repo (git clone <repo-url> cd <repo-folder)
2. Install Required Dependencies: "pip install -r requirements.txt"
3. Open the jupyter notebook
4. Run all the cells within the notebook


## Code Explanation/Workflow:

1. **Import Libraries**
   - We import the libraries for data manipulation (pandas, numpy), plotting (matplotlib), Modeling(sklearn), metrics r2_score, mean_absolute_error
   
2. **Load Dataset**
   - load_diabetes(as_frame=True) returns features x and target y
   - Features and target are explored for missing values and cleaned if it is needed to
   
3. **Exploratory Data Analysis**
   - Summary of statistics in: x.describe(), y.describe()
   - Correlation matrix: x.corr()
   - There are Visualizations in the form of histograms, scatter plots
4. **Train-Validation-Test Split** 
   - Split the dataset to ensure proper evaluation of models and avoid data leakage
5. **Univariate Polynomial REgression**
   - Polynomial features created using PolynomialFeatures
   - Models are evaluated for each degree using training and validation sets
   - Best model selected and plotted against train/validation/test data
   - Predict disease progression for chosen BMI
   - Trainable parameters are determined using get_feature_names_out()
   
6. **Multivariate Models**
   - Polynomial, Decision Trees, kNN, and Logistic Regression models fitted using multiple features.
   - Predictions generated for train, validation, and test sets


### Further Explanation of regression/alert rules: 
    - Polynomial regression captures nonlinear trends between BMI and disease progresion
    - Decsion trees and kNN allow for really flexible non-linear modeling with multiple features
    - Logistic Regression applied in a regression context using target scaling if necessary
    - MAPE, MAE, and R2 provide a comprehensive view of model accuarcy and reliability

🤝 Contributing
This is a Practical Lab developed for CSNC8010. If any questions arise do not hesitate to contact the project member.