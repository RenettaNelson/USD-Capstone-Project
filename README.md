# Airbnb Pricing Prediction
### Jacqueline Urenda
### Renetta Nelson
### July 3, 2023

## Objective

- The objective is to analyze seasonality and weather conditions that impact Airbnb price listings in San Diego as well as other factors guests take into consideration when booking such as area/neighborhood, reviews/ratings, listing counts, accommodation type, and more. The analysis of these features will determine an optimal pricing prediction model that Airbnb can implement to provide its new and existing hosts with pricing recommendations. 

## Data Sources

- Listings
- Calendar
- Reviews
- Neighbourhoods
- San Diego Weather

## Data Description

- Listings.csv: Contains property listing id numbers, listing names, descriptions, neighborhood overview, reviews, etc. The dataset contains a total of 12,871 instances and 75 features. 
- Calendar.csv: Contains property listing id numbers, listing date, availability, price, and min/max number of nights per stay. Dataset contains  4,697,550 rows of data and  7 features.
- Reviews.csv: Contains listing review information such as listing id, reviewer id, date, etc. This dataset contains 14,886 rows of data and 6 features.
- Neighbourhoods.csv: Contains neighborhood group and neighborhood name details. There are 108 rows of data and 2 features.
- SD_Weather_Data.csv: Contains weather details for the city of San Diego such as date, precipitation, air min, air max, and more. This dataset contains 2,369 rows of data and 6 features

## Methods Used

- Extract Data: Read CSV Files 
- Data Transformation/ Pre-Processing
- Load Data into SQL Table
- Data Analysis: Exploratory / Statistical
- Data Splitting: Training / Testing
- Models: Regression and Prediction
- Model Evaluation: RMSE and MAE

## Technologies

- Python
- SQL

## Required Libraries

- Pandas




