# Kaggle-House-Price-Solution



## Table Of Content
1. [Project Descriptiom](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview)<br>
    A. Problem Statement<br>
    B. Best Possible Solutions<br>
    C. Introduction About Project<br>
    D. Tools and Libraries
2. [Data Collection](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview)
3.  Generic Flow Of Project
4. [EDA_and_Model_Fit](https://github.com/kklsy109/Kaggle-House-Price-Solution/blob/main/Data_Processing.ipynb)<br>
    A. Data Cleaning<br>
    B. Feature Engineering<br>
    C. Data Normalization
    
  
  
### 1. Project background analysis
#### 1.1 Market and social factors affecting house prices

The purpose of conducting house price prediction is to estimate the cost of a property using specific details related to the property. This can greatly assist both buyers and sellers in making the wisest choices when buying or selling a house. It also provides valuable information about market trends and forecasts for investors and individuals involved in the real estate market.

Currently, there are many factors that can influence the price of a house, so we need to consider different features. These features include the size of the house, its location, accessibility to transportation, nearby amenities, age of the property, number of floors, style, and more. To predict the price, I will use a linear regression model to train these features and find their relationship with the price.

#### 1.2 House price data

Dataset: The dataset I have chosen is sourced from the Kaggle housing price prediction competition. This dataset includes the feature values for each transaction and the corresponding property prices.


#### 1.3 Model building and evaluation metrics

This project utilized linear regression and random forest methods for predicting housing prices, and validated the model's performance using mean squared error (MSE).

### 2. EDA


#### 2.1 Data Processing



In my original dataset, there are a total of 80 columns. I first analyzed the correlation between each attribute in the data and housing prices in order to eliminate some data that is not linearly related to housing prices. Then, I performed feature extraction and data cleaning on the remaining attributes.

![](https://github.com/kklsy109/Kaggle-House-Price-Solution/blob/main/Pictures/1.png)


##### 2.1.1 Feature Selection

I analyzed the factors influencing housing prices from two perspectives:

1) The impact of market factors on housing prices:
I created a chart combining histograms and line graphs to observe the differences in housing prices across different regions.

I compared the selling prices of houses horizontally and vertically based on the year and month of sale.

In addition, the year of construction of the property also has a certain influence on the housing prices.

I also created a heatmap illustrating the relationship between the year of construction and the location of properties in terms of housing prices.


2) The impact of real estate factors on house prices:
I have created scatter plots, box plots, histograms, and joint distribution plots to analyze the correlation between various real estate factors and house prices.


##### 2.1.2 Data Cleaning

Perform a log1p transformation on the target data to make its distribution closer to a standard normal distribution.


First, I convert the categorical data "MSSubClass" of numerical type into strings because its numerical values do not have a numeric meaning in themselves.





Then, I apply one-hot encoding to all the string data in the dataset, which will facilitate data fitting later.



#### 2.2 Data Standardization

I tried seven different methods for data normalization, and the z-score method performed the best in the end.



### 2. Model linear fit


First, I compared the Ridge, Random Forest, and Lasso models as target models, fitting each to the processed data.

Among the three models, I iterated the corresponding hyperparameters to tune the model parameters for the best results. In the iterative process, I chose cross-validation as the method to evaluate the model score and error rate. By plotting the hyperparameters and cross-validation scores, it can be observed that the model fit results can be locally optimized to the best.


1) Ridge Regression


2) Random Forest


3) Lasso


### 3. 






















