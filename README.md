# House-Price-Modelling 

Kaggle Link: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview

[Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/#contributing): This is the structure I am trying to
use for my projects based on a recommendation by a Senior Data Scientist at work.


## Personal Note
The purpose of this project is to further develop my skills in data science. This project serves as a starting point for a series of 
projects I want to complete to gain experience and further develop myself in this field. There are some core things I want to take away from
this project:

- Explore advanced regression techniques 
	- Research the theory 
	- Understand key assumptions 
	- Learn about the general processes 
- Brush up my data visualization & exploration skills 
- Learn more about best practices for version control in data science

## Introduction
The purpose of this project is create a model to predict the **sale price of houses** in Ames, Iowa; its an alternative to the common Boston Housing
dataset. The dataset was compiled by Dean De Cock, his guidelines for this project are available in the [References](References/) folder.
- Documentation for the different attributes in the dataset are also available in the References folder

**Project Objective:** Develop a model to predict sale prices for houses based on various numerical & categorical data
- Since this dataset is provides a good opportunity to investigate the properties of regression models, that will be the focus
	- In a real work environment, determining what type of technique to use beforehand is definetly not good practice
	
## Data Exploration

The training data consists of 1460 rows & 81 columns. 
- Based on the documentation by Dean De Cook, there are 23 nominal, 23 ordinal, 14 discrete, and 20 continuous features
- There are 19 attributes with empty/NULL values; the most being Alley (Type of alley access to property), FirePlaceQu (Fireplace quality),
PoolQC (Pool Quality), Fence (Fence Quality), and MiscFeature (Miscellaneous feature not covered in other categories).

### Multicollinearity

The VIF function was used to check for multicollinearity within the independent variables in this dataset. Based on this analysis a few variables were dropped.

- BsmtFinSF1, BsmtFinSF2, and BsmtUnfSF were dropped and only the TotalBsmtSF variable was retained
- 1stFlrSF and 2ndFlrSF were dropped off because they were highly correlated with GrLivArea
- GrLivArea still had a high VIF score of 8.2. Based on the heatmap, this could be caused by the correlation to the number of rooms and metrics related to garage size. However, since these could be real factors that impact the final sale price of a house, they were not removed.

### Missing Values

- PoolQC, MiscFeature, Alley, Fence, FireplaceQu, GarageType, GarageFinish, GarageQual, GarageCond, BsmtFinType1, BsmtExposure, BsmtFinType2, BsmtCond, BsmtQual, MasVnrType *all have NA meaning that the particular house 'feature' does not exist. The NAs do not represent true missing values*

## Reference Work

1. https://github.com/wblakecannon/ames/blob/master/ipynb/00-eda.ipynb
2. https://github.com/thisisclement/Ames-Housing-Price-Prediction/blob/master/code/proj_2_eda_modelling.ipynb
3. https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python
4. https://www.kaggle.com/masumrumi/a-detailed-regression-guide-with-house-pricing
5. Lot Frontage - https://www.kaggle.com/ogakulov/lotfrontage-fill-in-missing-values-house-prices

### Concepts 
1. Multicollinearity: https://www.analyticsvidhya.com/blog/2020/03/what-is-multicollinearity/
2. Multiple Regression: https://www.youtube.com/watch?v=AkBjJ6OunR4&t=631s
3. Variance_inflation_factor caveat when used to check for Multicollinearity: https://stackoverflow.com/questions/42658379/variance-inflation-factor-in-python
4. 





 