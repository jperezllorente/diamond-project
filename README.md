# DIAMONDS PROJECT

<p align="center">
  <img width="460" height="300" src="https://e3.365dm.com/20/10/2048x1152/skynews-diamond-stone_5154911.jpg">
</p>

## Overview

The objective of this project was to create four models that could predict the price of diamonds based 
on their characteristics, which were:

- id: only for test & sample submission files, id for prediction sample identification
- price: price in USD
- carat: weight of the diamond
- cut: quality of the cut (Fair, Good, Very Good, Premium, Ideal)
- color: diamond colour
- clarity: a measurement of how clear the diamond is
- x: length in mm
- y: width in mm
- z: depth in mm
- depth: total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)
- table: width of top of diamond relative to widest point (43--95)

The datasest can be found in the data folder of the repository.

## Resources and libraries
- pandas
- numpy

#### For visualization
- matplotlib.pyplot
- seaborn

#### For modeling 
- from sklearn.modelselection -> train_test_split, learning_curve, GridSearchCV, cross_validate and cross_val_score
- from sklearn.linearmodel -> LinearRegression
- from sklearn.tree -> DecisionTreeRegressor
- from sklearn.neighbors -> KNeighborsRegressor
- from sklearn.ensemble -> RandomForestRegressor, GradientBoostingRegressor

## Process and best model
After checking and cleaning the dataset, a series of models were trained: Linear Regression, Decision Tree, Random Forest and Gradient Boosting.
From this four models, the one that had a better (smaller) mean_squared_error was the Gradient Boosting model, with a MSE of 0.00801.

##  Future improvements
In order to improve the error I could have done more feature engineering, for example join x,y,z in just one variable (x*y*z) or I could have scaled the valuaes and trained a Kneighbor model. 

Also, I could have tried other options in the parametres used in the models in order to find a better fit.