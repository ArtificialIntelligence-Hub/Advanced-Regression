# Surprise Housing House Prediction
> A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.
 
## Table of Contents
* [Problem Statement](#problem-statement)
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## Problem Statement

### Business Understanding

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

### Business Goal:

You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

### Business Risk:

- Anticipating a higher sale price for a house may fail to attract potential customers, thereby potentially resulting in a loss for the company.

- Conversely, forecasting a lower sale price for a house could result in a reduction of the company's profit margin.

### Requirement:

- Which variables are significant in predicting the sale price of the house?
- To what extent do those variables effectively describe the sale price of the house?

## General Information
- Steps for crreating a Regularized regression model :
<ol>
    <li>Data Visualization</li>
      <ol>
        <li>Perform EDA to understand various variables.</li>
        <li>Check the correlation between the variables.</li>
      </ol>
    <li>Data Preparation</li>
      <ol>
        <li>Create dummy variables for all the categorical features.</li>
        <li>Divide the data to train & Test.</li>
        <li>Perform Scaling.</li>
        <li>Divide data into dependent & Independent variables.</li>
      </ol>
    <li>Data Modelling & Evaluation</li>
      <ol>
        <li>Create Linear Regression model using RFE</li>
        <li>Create L1 and L2 Regularized Models using the output of the RFE</li>
        <li>Check the various assumptions.</li>
        <li>Check the Adjusted R-Square for both train & Test data.</li>
        <li>Report the final model.</li>
      </ol>
</ol>
- Data Set : train.csv 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
**Conclusion of Exploratory Data Analysis (EDA):**

**Continuous Variable Insights:**

- LotFrontage: SalePrice tends to increase with an increase in LotFrontage within the range of 20.7 to 196.2.
- LotArea: SalePrice generally increases with larger LotArea within the range of 1086 to 65483.
- MasVnrArea: SalePrice tends to rise with an increase in MasVnrArea within the range of 0 to 1280.
- BsmtFinSF1: SalePrice increases with an increase in BsmtFinSF1 within the range of 0 to 2257.
- BsmtFinSF2: There's minimal effect on SalePrice with an increase in BsmtFinSF2.
- BsmtUnfSF: SalePrice tends to increase with larger BsmtUnfSF within the range of 1168 to 2336.
- TotalBsmtSF: SalePrice generally increases with larger TotalBsmtSF within the range of 0 to 3666.
- 1stFlrSF, 2ndFlrSF, GrLivArea: SalePrice tends to increase with larger values of these variables.
- GarageYrBlt: There's minimal effect of GarageYrBlt on SalePrice.
- GarageArea: SalePrice generally increases with larger GarageArea within the range of 0 to 1276.
- WoodDeckSF: SalePrice tends to increase with an increase in WoodDeckSF within the range of 0 to 685.
- OpenPorchSF, EnclosedPorch: There's minimal effect of these variables on SalePrice.
- AgeBuilt, AgeRemod: SalePrice decreases with an increase in AgeBuilt and AgeRemod initially, then slightly increases.

**Categorical Variable Insights:**

- Various categorical variables such as MSSubClass, MSZoning, LotShape, LandContour, LotConfig, Neighborhood, Condition1, BldgType, HouseStyle, Exterior1st, Exterior2nd, MasVnrType, ExterQual, Foundation, BsmtQual, BsmtCond, BsmtExposure, BsmtFinType1, BsmtFinType2, HeatingQC, FullBath, HalfBath, BedroomAbvGr, KitchenQual, TotRmsAbvGrd, Fireplaces, FireplaceQu, GarageType, GarageFinish, GarageCars, GarageQual, SaleType, and SaleCondition show variations in SalePrice across different categories.

**Significant Predictors of House Price:**

- 'OverallQual_10'
- 'OverallQual_9'
- 'Neighborhood_NoRidge'
- 'FullBath_3'
- 'TotRmsAbvGrd_11'
- 'Fireplaces_3'

**Model Evaluation:**

The significance and effectiveness of the predictors in describing the house price are as follows:

- OverallQual_10: 0.833928
- OverallQual_9: 0.830237
- Neighborhood_NoRidge: 0.592742
- FullBath_3: 0.530678
- TotRmsAbvGrd_11: 0.505044
- Fireplaces_3: 0.442772

**Optimal Regularization Values:**

For Ridge Regression: 6.0

For Lasso Regression: 0.001

**Final Model Selection:**

The Lasso Regularized model is chosen as the final model for predicting SalePrice due to the following reasons:

- It offers more feature elimination, leading to a simpler, more robust, and generalized model.
- It demonstrates similar performance compared to Ridge Regularization.

This choice ensures a balance between predictive power and model simplicity, enhancing its utility in real-world applications.
## Technologies Used
- pandas - 1.3.4
- numpy - 1.20.3
- matplotlib - 3.4.3
- seaborn - 0.11.2
- plotly - 5.8.0
- sklearn - 1.1.2
- statsmodel - 0.13.2


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was group case study for an online advance course.
- https://www.geeksforgeeks.org/
- https://seaborn.pydata.org/
- https://plotly.com/
- https://pandas.pydata.org/
- https://learn.upgrad.com/


## Contact
Created by [@ArtificialIntelligence-Hub] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
