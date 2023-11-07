# Milano House Price Estimator: Project Overview 
* Created a tool that estimates the prices of houses in Milano, Italy.
* Scraped 2000 announcements from immobiliare.it using python.
* Engineered features from each announcements. 
* Optimized Linear Regression, Support Vector Regressor, Decision Tree Regressor, and Random Forest Regressors using GridsearchCV to reach the best model.

## Code and Resources Used 
**Python Version:** 3.11  
**Packages:** pandas, numpy, sklearn, scipy, matplotlib, seaborn, pickle, BeautifulSoup

## Web Scraping
Scraped 2000 apartment announcements from immobiliare.it. With each announcements, we got the following:

*	Price in Euros
*	Number of rooms
*	Surface area in meter-squared
*	number of bathrooms
*	Floor number
*	Announcements description
*	Reference and Listing date
*	City
*	Neighborhood
*	Street
*	.......etc.

## Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

* Removed columns with null values bigger than half the length of dataset.
*	Extracted numeric data out of price_euro column.
*	Dropped rows with no price.
*	Extracted the right number of rooms from rooms column.
*	Extracted the right surface area from surface column.
*	Extracted the right number of bathrooms from rooms column.
*	Extracted the right floor number floor_number column.
*	Extracted numeric data out of total building floors column.
*	Extracted numeric data out of condominium fees column.
*	Filled the null values of condominium fees with the mean of each neighborhood.
*	Made new columns:
    * with_disabled_access
    * with_lift
    * listing Date
    * price_m2

## EDA
* I looked at the distributions of the data.
* The value counts for the various categorical variables.
* Correlation heatmap.
* I removed Outliers.
* Dealing with skewed data.
  
![alt text](https://github.com/amraskar/Milan-Housing-Prices-Prediction/blob/3a69e349ea8d2de2c29f9d9998d8a8b998dda2ef/ads.png "Number of announcements in each neighborhood")
![alt text](https://github.com/amraskar/Milan-Housing-Prices-Prediction/blob/3a69e349ea8d2de2c29f9d9998d8a8b998dda2ef/prices.png "Average prices in each neighborhood")
![alt text](https://github.com/amraskar/Milan-Housing-Prices-Prediction/blob/3a69e349ea8d2de2c29f9d9998d8a8b998dda2ef/heatmap.png "Correlation heatmap")
![alt text](https://github.com/amraskar/Milan-Housing-Prices-Prediction/blob/3a69e349ea8d2de2c29f9d9998d8a8b998dda2ef/Distribution.png "distributions")
![alt text](https://github.com/amraskar/Milan-Housing-Prices-Prediction/blob/3a69e349ea8d2de2c29f9d9998d8a8b998dda2ef/boxplot.png "boxplot")
