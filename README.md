# Predictive_Performance_Analysis_of_Airbnb_Metrics
Dissertation
# Project Overview
The aim of this project is to predict an Airbnb price predictive model and to also buld a recommendation system
That would help property owners in looking to invest in the shortlet business via the Airbnb platform.
# Models
Two different models were used Regression Models and Colaborative Filtering

## Regression Models
Four different models were experimented on with Linear regression model being the benchmark after which more complex
models like Decision Tree, Random Forest and XGBoost were also introduced for better performance.
XGBoost out performed the rest with an R2 score of 0.72. Which means 72% of the variance predicted price.

## Colaborative Filtering model
The model based approached was used for this recommendation system, where algorithm such as BaselineOnly, SlopeOne and SVD
was experimented on. With SVD out performing the rest algorithms with an RMSE of 0.4097.
