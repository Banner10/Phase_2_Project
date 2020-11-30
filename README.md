# Introduction

This repository represends a linear regression model that can be used to predict the housing prices for King County, Washington. A copy of the raw data can be found within this repository under the title of 'kc_house_data.csv'. The data contains over 21000 house sales from 2014 and 2015. The raw column information can be found below:

### Column Names and descriptions for Kings County Data Set
* **id** - unique identified for a house
* **dateDate** - house was sold
* **pricePrice** -  is prediction target
* **bedroomsNumber** -  of Bedrooms/House
* **bathroomsNumber** -  of bathrooms/bedrooms
* **sqft_livingsquare** -  footage of the home
* **sqft_lotsquare** -  footage of the lot
* **floorsTotal** -  floors (levels) in house
* **waterfront** - House which has a view to a waterfront
* **view** - Has been viewed
* **condition** - How good the condition is ( Overall )
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - Built Year
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors

# Note Books Included in Repository:

* **Baseline_Model** - Baseline model for raw data
* **House_Cleaned** - Data Cleaning and EDA
* **Visualization** -  Visualizations Used for Presentation
* **Model_919** -  Final model training
* **Presentataion** -  Non-Technical Presentation
* **house_cleaned.csv** - Cleaned Data used for final model

# Description of Work:

## Goals / Defining Problem:

To build an ordinary least squares or OLS liniar regression moedel to accuratly predict housing prices in King County.  This model can be used by real estate agents, developers, buyers, and sellers. Most accuratly used for houses that lie close that are averagly priced for the county.    

## Process:

### Baseline Model:

The process begins with establishing a baseline model. This model takes into account all data points and uses price as the independent variable as we will throughout the mdoeling process. The R-squared value for this baseline model was .699 with a Root Mean Square Error(RMSE), $198314.69.

### Data Cleaning / EDA:

The cleaning of data first included becoming familiar with the data. Exploring the columns and identifying key metrics. We decided to add an important metric for pricing houses of Price Per Square Foot. After that we decided to drop the id, date, and year renovated columns as they were deemed unnecessary. The next step was to remove all significant outliers, because this is a price driven model we began with price. Removing all outliers that were outside of two standard deviations of the mean allows us to focus out model on our target audience of the average home buyer in the county. We then proceeded to remove all significant outliers for bedrooms, bathrooms, and floors. Scatter plots were used to confirm. 

### Final Model:

When training my final model, we began by exploring correlation. We used a heat map to visually examine the relationships. Next we decided to consider the zip code column as categorical as it was the only non-continuous column. We one hot encoded into dummy variables for all 70 zip codes. Logically, we then checked for collinearity. Dropped square foot above as it was a redundant column and moved into future selection. Feature selection was done using a p-table summary along with a stepwise function.  About 20 features were removed as they had p-values higher than .05 and were deemed statistacally insignificany.

### Final Model Results:

The Final model has a R-squared value of .919 and a RMES of $52809. These results were more than acceptable and allowed us to determine the relationship to price for each significant variable along with each significant zip code by examining the coefficients for each. 





