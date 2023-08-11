# Wine Quality Prediction

## Overview

This project aims to predict the quality of red wine based on various physicochemical properties such as fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol. The dataset contains 1599 examples, each with 11 features and 1 target variable (quality). The quality is an ordinal variable that ranges from 0 (very bad) to 10 (very excellent).

## Data Cleaning and Exploration

The data cleaning and exploration process was done using numpy, pandas, seaborn, plotly.express, and matplotlib libraries in Python. The following steps were performed:

- Imported the libraries and ignored the warnings
- Read the csv file into a pandas dataframe
- Displayed the first 5 rows of the dataframe
- Printed the column names of the dataframe
- Checked the shape and information of the dataframe
- Checked the null values and unique values of the dataframe
- Checked and dropped the duplicated values from the dataframe
- Displayed the summary statistics of the dataframe
- Plotted a heatmap to show the correlation matrix of the dataframe
- Split the dataframe into features (X) and target (Y)
- Split the features and target into train and test sets with a test size of 0.3 and a random state of 42
- Printed the shape of each set
- Plotted histograms to show the distribution of each feature using a loop

## Data Modeling and Evaluation

The data modeling and evaluation process was done using scikit-learn library in Python. The following steps were performed:

- Imported the LinearRegression model from scikit-learn
- Created an instance of the model
- Trained the model using the train set
- Made predictions on the train set using the model
- Imported the metrics module from scikit-learn
- Evaluated the model on the train set using mean absolute error (MAE), root mean squared error (RMSE), and R-squared metrics
- Printed each metric value for the train set
- Made predictions on the test set using the model
- Evaluated the model on the test set using MAE, RMSE, and R-squared metrics
- Printed each metric value for the test set
- Imported the cross_val_score function from scikit-learn
- Performed 5-fold cross-validation on both train and test sets using R-squared, mean squared error (MSE), and root mean squared error (RMSE) as scoring metrics
- Calculated and printed the mean value of each metric for both sets

## Conclusion

This project demonstrates how to use various tools and techniques to clean, explore, model, and evaluate a dataset of wine quality. The results reveal some interesting insights into the wine industry, such as:

- The target variable (quality) had a skewed distribution with most wines having a quality score between 5 and 6, indicating that most wines were average in quality while few wines were very good or very bad
- The features had different ranges, scales, and distributions, some of them showing outliers or skewedness
- The correlation matrix showed that quality had a moderate positive correlation with alcohol, a moderate negative correlation with volatile acidity, and a weak positive correlation with sulphates and citric acid
- The histograms showed that some features such as fixed acidity, residual sugar, free sulfur dioxide, total sulfur dioxide, sulphates, and alcohol had long right tails, indicating that they had some extreme values or outliers
- The LinearRegression model achieved an MAE of 0.50, an RMSE of 0.65, and an R-squared of 0.36 on the train set; and an MAE of 0.52, an RMSE of 0.68, and an R-squared of 0.33 on the test set; indicating that it was able to explain only about one-third of the variance in quality
- The cross-validation results showed that there was not much difference between the train and test sets in terms of R-squared, MSE, and RMSE; indicating that there was no overfitting or underfitting problem
