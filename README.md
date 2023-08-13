# Airbnb Pricing Prediction
### Jacqueline Urenda
### Renetta Nelson
### Michael Nguyen
### August 14, 2023

## Objective

- The objective is to analyze seasonality and weather conditions that impact Airbnb price listings in San Diego as well as other factors guests take into consideration when booking such as area/neighborhood, reviews/ratings, listing counts, accommodation type, and more. The analysis of these features will determine an optimal pricing prediction model that Airbnb can implement to provide its new and existing hosts with pricing recommendations. 

## Data Sources

- Listings (Note: this dataset was too large to upload to GitHub. Dataset can be accessed through this link https://drive.google.com/file/d/1gGo0dX07-SVReIo_BWyF4CgvalGULfaq/view?usp=share_link) 
- Calendar
- San Diego Weather

## Data Description

- Listings.csv: Contains property listing id numbers, listing names, descriptions, neighborhood overview, reviews, etc. The dataset contains a total of 12,871 instances and 75 features. 
- Calendar.csv: Contains property listing id numbers, listing date, availability, price, and min/max number of nights per stay. Dataset contains  4,697,550 rows of data and  7 features.
- SD_Weather_Data.csv: Contains weather details for the city of San Diego such as date, precipitation, air min, air max, and more. This dataset contains 2,369 rows of data and 6 features

## Methods Used

- Extract Data: Read CSV Files 
- Data Transformation/ Pre-Processing
- Data Analysis: Exploratory / Statistical
- Data Splitting: Training / Testing
- Models: Regression and Prediction
- Model Evaluation: RMSE and MAE

## Technologies

- Python


## Required Libraries

- pandas
- numpy
- random
- xgboost
- sklearn.tree
- sklearn.metrics
- sklearn.ensemble
- matplotlib

## Abstract 

Airbnb has become a booming opportunity for businesses and individuals to list their properties and make revenue. As the Airbnb market can often fluctuate, it can be challenging for hosts to determine an optimal pricing strategy for their listings. It is important to understand all the factors that can contribute to such variability in listing prices to identify an optimal pricing strategy for each unique neighborhood or listing. Related projects were reviewed to demonstrate how this project can contribute to existing research. The methodology involved identifying the problem, determining an approach to solving that problem, acquiring the data, prepping the data, training and testing specific models, evaluating the performance, deploying the model, and obtaining feedback. Exploratory Data Analysis was conducted. The following datasets were initially extracted: calendar, weather, and listings. These datasets were then merged into a final dataset that will be used for modeling. During the preprocessing stage, the dataframes’ null values were resolved, data types were converted to the correct format, and unnecessary features were dropped. In the subsequent step of test design, the goal is to create robust training and validation datasets. These datasets are instrumental in training the model and in assessing its predictive performance. The models included are decision tree, XGBoost, and random forest. To determine the effectiveness of these models, various statistical indicators such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2), Adjusted R-squared, and Mean Absolute Percentage Error (MAPE) were computed. The results imply Random forest is the best fit model. For future studies, there could be further optimization of the models. GridSearch tests different combinations of model parameters until it finds the best one. Cross Validation can also be implemented. Taking the cross-validation error can reduce the chance of overfitting. Other methods, such as Random Search and Bayesian Optimization, can be used as well.


## Business Background 

Numerous factors can directly contribute to the pricing of an Airbnb listing. Specifically, within the lodging industry, prices can fluctuate daily depending on several factors such as day of the week, month, weather conditions, and more. Even a city with a great reputation for weather, like San Diego, could have travel volume changes based on the time of year and weather conditions. According to the US News & World Report, San Diego’s peak season for travel is from June through August. However, rainy conditions such as “June Gloom” can dissuade travelers from going during its early “high season.” With change in volume of travelers also comes change in demand pricing. These factors can greatly affect the price of Airbnb listing prices for the city of San Diego. 


## Problem Statement 

Aside from seasonality and weather, location and amenities can greatly affect the price of an Airbnb listing as well. There are numerous neighborhoods within the city of San Diego that can have different pricing brackets. For instance, a listing near a highly demanded neighborhood like Pacific Beach which offers easy access to restaurants, bars, and beaches could be more expensive than other areas that may not have such proximity to points of interest. It is important to understand all the factors that can contribute to such a variability of listing prices to be able to identify an optimal pricing strategy for each unique neighborhood or listing. 

## Summary of the findings 

After splitting the dataset, we selected several regression models to fit the training dataset. They were the decision tree, XGBoost, and random forest. The models' performance was evaluated based on various metrics. The R^2 value, representing the square of the correlation coefficient R, measures the variability of the features. A higher R^2 value indicates that the model's predictions align more closely with the actual data values. However, the potential for overfitting necessitated the inclusion of the adjusted R^2 in our evaluation. RMSE, the square root of the mean squared error, is another crucial metric we analyzed. A model with a lower RMSE suggests fewer prediction errors and is indicative of better performance. Lastly, the MAPE metric was used which represents the mean absolute percentage error of the model. A lower MAPE is preferable in this case. It shows that, on average, the model's predictions are closer to the actual values.


## Business Questions 

What features contribute to the variability of listing prices? Which model would provide the most optimal results for price prediction? What are the key performance indicators that will measure the accuracy and precision of the models?

## Scope of analysis 

Numerous features were removed front the dataset. Only the features related to pricing were kept in the final dataset. 

## Approach 

Our methodology is to identify the problem, determine an approach to solving that problem, acquire the data, prep the data, train and test on specific models, evaluate the performance, deploy the model, and obtain feedback. The next step in the process was to select suitable models to train on the dataset. After the data preparation process, the dataset was quite large and had over 3 million instances. Since there were multiple listings within the dataset, the appropriate models and techniques would need to be implemented to forecast pricing for multiple listings. The regression models were selected based on the complexity of the dataset as well as their speed and notable performance compared to other regression models. In the process of selecting suitable modeling techniques, we began by making a benchmark model using the Decision Tree Regressor. This model was trained with the final merged and cleaned dataset. Following this, we implemented an XGBoost Regression model, which evaluated in a manner like the decision tree regressor that demonstrates an improvement in the performance metrics. We also utilized an ARIMA model to forecast prices. Once trained, the model was leveraged to generate a forecast. In addition, we introduced a Linear Regression model to the final dataset and assessed its performance through the calculation of the variance score. To further bolster our modeling efforts, we selected a random subset from the final dataset and deployed a RandomForestRegressor model as a starting point. We employed hyperparameter tuning with the help of the RandomizedSearchCV method to identify the best hyperparameters, leading to the development of an enhanced RandomForestRegressor model. To determine the effectiveness of the models, we computed various statistical indicators such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2), Adjusted R-squared, and Mean Absolute Percentage Error (MAPE). These provided a preliminary assessment of the model's performance. 

 
## Limitations 

A limitation of the project would be that it only applies to one city. Ideally, it would be scaled to other areas as well. In addition, more advanced models could have been implemented as well. 


## Solutions Details

From the evaluation, the Random Forest model, with the lowest MAPE of 0.1682, emerged as the best performer in terms of average percentage error. Even though the Decision Tree presented the smallest MSE and RMSE and had an equally high R^2 value, the significantly lower MAPE of the Random Forest indicated that its predictions were, on average, closer to the actual values.
Thus, the Random Forest model was our choice. This predictive tool will be extremely useful for Airbnb hosts, guiding them in determining optimal pricing for their listings with minimized error. It ensures that hosts are making informed pricing decisions for their listings.




## Concluding Summary 

With change in volume of travelers also comes change in demand pricing. These factors can greatly affect the price of Airbnb listing prices for the city of San Diego. It is important to understand all the factors that can contribute to such a variability of listing prices to be able to identify an optimal pricing strategy for each unique neighborhood or listing. The R^2 value, representing the square of the correlation coefficient R, measures the variability of the features. RMSE, the square root of the mean squared error, is another crucial metric we analyzed. The MAPE metric was used which represents the mean absolute percentage error of the model. Numerous features were removed front the dataset. Only the features related to pricing were kept in the final dataset. Our methodology is to identify the problem, determine an approach to solving that problem, acquire the data, prep the data, train and test on specific models, evaluate the performance, deploy the model, and obtain feedback. A limitation of the project would be that it only applies to one city. Ideally, it would be scaled to other areas as well. Even though the Decision Tree presented the smallest MSE and RMSE and had an equally high R^2 value, the significantly lower MAPE of the Random Forest indicated that its predictions were, on average, closer to the actual values. Thus, the Random Forest model was our choice. 


## Call to action (CTA) 

Setting the right price for Airbnb listings in San Diego presents a challenge due to varying factors. Weather conditions, tourist seasons, and local attractions can significantly influence pricing decisions. A vast amount of data was analyzed, and several methods were tested to find an optimal pricing strategy. The Random Forest model emerged as the most accurate tool for determining suitable prices for listings across different San Diego neighborhoods. Using the Random Forest model can assist in achieving optimal pricing, which balances profitability with market demand. Understanding the factors that influence price fluctuations, such as weather changes or peak tourist times, ensures competitive pricing. Although this research is focused on San Diego, the model's principles might apply in other cities as well. For San Diego hosts, the Random Forest model offers a very powerful tool that can be used for informed pricing decisions. Ensuring that listings are neither underpriced or overpriced can be pivotal for success. Researchers or tech enthusiasts might explore the methodology in detail and consider its application in other cities or its enhancement through other models. Business strategists or consultants can leverage these insights to guide pricing strategies, adding value to the services offered to Airbnb hosts. Utilizing data-driven tools like the Random Forest model offers an effective strategy for determining optimal Airbnb pricing.



