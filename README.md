# Introduction

This repository represends a linear regression model that can be used to predict the housing prices for King County, Washington. A copy of the raw data can be found within this repository under the title of 'kc_house_data.csv'. The data contains over 21000 house sales from 2014 and 2015. The raw column information can be found below:

#### Column Names and descriptions for Kings County Data Set
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

# Description of Work:

## Goals:

We are building an Ordinary least Squares or OLS liniar regression moedel to accuratly predict housing prices in KC.  This model can be used my real estate agents, real estate developers, buyers, and sellers. 

All data except date column are numeric other than Zipcode which we will classify as categorical.  The categorical columns will need to be one hot endcoded into numerical values. will need to be dummified as it's one of our neighborhood proxies and not a continuous numeric value.