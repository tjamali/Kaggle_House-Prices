Kaggle: House Prices Competition
=============

####  Competition Description

![competition logo](https://storage.googleapis.com/kaggle-competitions/kaggle/5407/media/housesbanner.png)

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

#### What we do

Here, I use the simple Linear Regression method to predict homes price. I will go through the following four steps:

1. Download the data
2. Explore the data and Feature engineering
3. Build a model
4. Make a submition file

### Step 1: Download the data

At the first step we need to download the competition [data](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). 

#### File descriptions
- train.csv - the training set
- test.csv - the test set
- data_description.txt - full description of each column, originally prepared by Dean De Cock but lightly edited to match the column names used here
- sample_submission.csv - a benchmark submission from a linear regression on year and month of sale, lot square footage, and number of bedrooms

It is very useful to take a look at data_description.txt file that contains all information about the features in this competetion.

The test.csv file contains 80 features, while train.csv file has 81 features. The difference comes forom this fact that the test data does not have the  sale price column!

### Step 2: Explore the data and Feature engineering

The main aim is to predict the sale price of the homes. In the training data set, the SalePrice column shows this information which is the target variable.

After analyzing data, we obtain useful information about the data. For instance, we will find that home price distribution is positively skewed. Since, we are going to use Linear Regression method and the data are skewed, it is better to take logarithm of the price values for getting more precise predictions.

Some useful mini steps are:

- Dealing with numeric features
 (We will find most correlated (positive/negative) features with sale prices and removing outliers)
- Dealing with null values
- Dealing with non-numeric features
- Transforming and engineering features
(We will use one-hot encoding to transform some non-numeric columns into a numeric ons)

### Step 3: Build a linear model

At this step, we prepare the data for modeling by seperating the features and the target variable.


