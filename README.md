# Bike_Sharing_Demand_Prediction

## Project Summary -
The project involved building and evaluating different regression machine learning models for predicts the count of bike rentals, such as linear regression, Ridge regression, Lasso regression, ElasticNet regression, and RandomForest regression. The models were trained and evaluated using various metrics such as MSE, RMSE, R2, and Adjusted R2 on both the training and test datasets.

The RandomForest model demonstrated the best performance without overfitting, as it exhibited lower MSE and RMSE values, higher R2 values (Training dataset - 0.984354, test datasets - 0.895198) and high Adjusted R2 values (training datasets -0.894506 , test datasets - 0.892371) on both the training and test datasets.

RandomForest model is also explained with the help of shap library.

## Problem Statement
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.


## Conclusion

### EDA Insight:

#### Distribution Wise :
* Right Skewed : Rainfall, Snowfall and Solar_radiation
* Left skewed : Visibility
* Normal : Temperature and Humidity

#### Rental Bike Pattern :
1. Bike rentals are highest when the temperature ranges between 25-30 degrees Celsius.
2. The number of bike rentals decreases as humidity increases.
3. Bike demand remains relatively stable across different wind speeds, but there is a slight increase at 7 m/s.
4. Rainfall has a limited impact on bike rentals, while heavy snow negatively affects demand.

#### Correlation with dependent variable :
* Positive Correlation : Temperature, Dew_point_temperature and solar_radiation.
* Negative correlation : Humidity, Rainfall and snowfall.

#### Time and Seasonal Patterns:
1. The highest bike rentals occur during working hours, from 7 am to 9 am and 5 pm to 7 pm.
2. Summer has the highest bike rental demand, followed by Autumn.
3. Bike rentals significantly decrease during holidays and non-functioning days.
4. Bike rentals are highest from May to October and lowest in December, January, and February.
5. Weekdays have significantly higher bike rentals compared to weekends.

### ML Models:

![Screenshot 2023-07-02 181512](https://github.com/manish021996/Bike_Sharing_Demand_Prediction/assets/120492463/e76dbbed-075d-40c0-b2c1-fabc41369bfa)


* Among the evaluated models, the RandomForest and RandomForest with GridSearchCV model shows the best performance with lower MSE and RMSE values, higher R2 values, and high Adjusted R2 values on both the training and test sets.
* It outperforms the ElasticNet, Ridge, and Lasso models, which exhibit slightly higher errors and lower R2 values.
* No sign of overfitting seen.
* Therefore, the RandomForest model and RandomForest with GridSearchCV is recommended as the top choice for this regression task.
* Important features : Functioing_day_Yes, Temperature, Humidity, Rainfall, Hour 4, 5.


