# Ames Housing Data and Kaggle Challenge

### Problem Statement
Accurately predicting the sale price of a home by building a machine learning Regression Model based on the features of the home.

**Primary Objectives:**
1. Creating and iteratively refining a regression model
2. Using [Kaggle](https://www.kaggle.com/) to practice the modeling process
3. Providing business insights through reporting and presentation.

This repo contains data and my process in creating a regression model based on the Ames Housing Dataset. This model will predict the price of a house at sale.

The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 70 columns of different features relating to houses. I participated in the Kaggle competition to give myself the opportunity to practice the following skills:

- Refining models over time
- Use of train-test split, cross-validation, and data with unknown values for the target to simulate the modeling process
- The use of Kaggle as a place to practice data science

A presentation is included in this repo.
**NOTE: The best model for Kaggle is not the best model to address your data science problem.**

## The Modeling Process

1. The train dataset has all of the columns that are needed to generate and refine the models. The test dataset has all of those columns except for the target that I am trying to predict in the Regression model.
2. Generate my regression model using the training data. Expected in this process:
    - train-test split
    - cross-validation / grid searching for hyperparameters
    - strong exploratory data analysis to question correlation and relationship across predictive variables
    - code that reproducibly and consistently applies feature transformation (such as the preprocessing library)
3. Predict the values for my target column in the test dataset and submit my predictions to Kaggle to see how the model does against unknown data.

4. Evaluate models!
    - consider evaluation metrics
    - consider baseline score
    - how can the model be used for inference?
    - why do I believe the model will generalize to new data?


### Our Dataset
We are given a training dataset and a testing dataset to use. There are many variables within the set spanning the gamuts of categorical, ordinal and numerical. These features contain a lot of noise and missing null values but also valuable signal and insight.

### EDA
To begin I loaded, explored and cleaned the training data. I dropped unnecessary, low correlated and high null columns. Ordinal variables were converted to numerical and appropriately ranked. I engineered features and created interactions where collinearity was found. I visualized the data and dropped outliers.

### Modeling
Linear Regression was my initial model. I logged the y variable due to its skewness and used the Standard Scaler on the X data. Ridge and Lasso Regression were incorporated as well. Everything was scored using R2 and Cross Validation. My method was simply manual trial and error of model testing with different feature combinations and amounts.

### Conclusion:
Not surprisingly, the sale price of a home is positively correlated with Total Square Footage and the Overall Quality of the home in many categories such as Kitchen, Exterior, Basement etc. I recommend for anyone investing or selling to keep these insights in mind and to possibly explore other areas of intrigue such as possible correlation of neighborhood and encoding other categorical variables.
