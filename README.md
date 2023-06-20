# Rossmann Store Sales Prediction 
AlmaBetter Verified Project

![image](https://github.com/Shubham-droid24/Rossmann-Store-Sales-Prediction/assets/72461022/48c12c74-5565-49ba-8534-b4dd6349f71b)


I have built machine learning models for solving regression problem to predict the daily sales of rossmann stores. I have used Linear Regression, Decision Tree Regressor and Random Forest Regressor algorithms to solve the problem and got the best results from Random Forest Regressor.

## Problem Statement

Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

In this project, you are provided with historical data of 1,115 Rossmann stores and you have to forecast 'Sales' column. Note that some of the stores were temporarily closed for refurbishment.




## Why do we need to do this project?

Businesses use sales forecast to determine what revenue they will be generating in a particular timespan to empower themselves with powerful business plans and strategies. Important decisions such as budgets, hiring, incentives, goals, acquisitions and various other growth plans are affected by the revenue the company is going to make in the coming months and for these plans to be as effective as they are planned to be it is important for these forecasts to also be as good.

Sales forecasting refers to the process of estimating demand or sales of a particular product over a specific period of time. Sales forecasting is the process of estimating a company’s sales revenue for a specific time period – commonly a month, quarter, or year. Basically,a sales forecast is prediction of how much a company will sell in the future.

This project involves solving a real-world business problem of sales forecasting and building up machine learning models for the same.

## Summary

I have summarized the project in 4 steps that how the flow of the project goes:-

First, I understood the Rossmann stores data having two datasets i.e Rossmann Store and Store. We are provided with historical data of 1,115 Rossmann stores in both datasets which were having different columns and one common so, I understood all the variables and how they can be important to the target variable i.e Sales.

Second, I merge the two datasets for furthur analysis and extracting Year,Month,Day of year and Week of year from the Date column in order to use them for visualization purpose. In visualization, I started from univariate analysis to bivariate and multivariate analysis and in every visualization comparing sales with other variables in order to understand the relation and impact or importance of them. From the visualization, I defined and tested three hypothesis and rejected all of them as p-value was less than significance level.

Third, I have done preprocessing which is important before model implementation. In this, I handled missing values and outliers , encoding the categorical variables, some feature engineering done to create new features and remove old ones, feature selection on the basis of correlation and multicollinearity. After having selection of important features I transformed some of them, done data splitting and feature scaling. All these were important to be done as they create a great impact on the model performance.

Last, I build different models and forecasted the sales for the various Rossmann stores across Europe for the recent six weeks and compared the predicted sales values of different models developed and implemented with the actual sales values. Also, I found out the factors and the most important features required to predict and influence the sales of Rossmann stores.

## Conclusion

Some important conclusions drawn from the project are as follows:

### From Visualization:

1) Most stores have competition distance within the range of 0 to 10 kms and had more sales than stores far away probably indicating competition in busy locations vs remote locations.

2) The positive effect of promotion on Customers and Sales is observable.

3) There were more sales on Monday, probably because shops generally remain closed on Sundays which had the lowest sales in a week.

4) Store type B though being a few in number had the highest sales average. The reasons include all three kinds of assortments specially assortment level b which is only available at type b stores and being open on sundays as well.

5) he outliers in the dataset showed justified behaviour. The outliers were either due to store type b or had promotion going on which increased sales.

### From Hypothesis Testing :

1) Average Sales of stores having competition distance upto 10 km is greater than that of stores which are far away(having competition distance greater than 10 km.
2) Average Sales of Store Type 'b' is greater than that of Store Type 'a'.
3) Average Sales of Stores having promotion applied i.e Promo = 1 is greater than that of Stores having no promotion applied i.e Promo = 0.

### From Model Implementation :

Random Forest Model using hyperparameter optimization technique(GridSearchCV) gave the best result of R^2 value on test data i.e 0.8353 and only 0.49% improvement was seen from the basic random forest model which indicates that most of the trends and patterns that could be captured by this model without overfitting was done and certainly, a good level of performance was achieved by the model.

### From Model Explainability(using LIME) :

The 5 most important features in predicting the sales of a store on a particular day are :

Promo, Store Type, Day of Week, Assortment and Promo2
