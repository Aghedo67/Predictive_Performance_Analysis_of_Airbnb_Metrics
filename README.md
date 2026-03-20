# Predictive_Performance_Analysis_of_Airbnb_Metrics
Dissertation
# Project Overview
The aim of this project is to predict an Airbnb price predictive model and to also buld a recommendation system
That would help property owners in looking to invest in the shortlet business via the Airbnb platform.
# Models
Two different models were used Regression Models and Colaborative Filtering
 Model
R2 score
Train MAE 
Test MAE
Train RMSE
Test RMSE
LR
0.5815
0.3337
0.3530
0.2007
0.2034
Decision Tree
0.6416
0.2824
0.3229
0.1407
0.1742
Random Forest
0.7118
0.1022
0.2784
0.0208
0.1401
XGBoost
0.7173
0.1446
0.2803
0.0360
0.1374

## Regression Models
Four different models were experimented on with Linear regression model being the benchmark after which more complex
models like Decision Tree, Random Forest and XGBoost were also introduced for better performance.
XGBoost out performed the rest with an R2 score of 0.72. Which means 72% of the variance predicted price.

 XGBoost learning curve
 	 XGBoost A & C price
 
<img width="468" height="229" alt="image" src="https://github.com/user-attachments/assets/1f6a2be9-78f6-4122-9a20-139b82cd5f21" />



 
<img width="468" height="224" alt="image" src="https://github.com/user-attachments/assets/920b8d8a-5d78-42a2-a366-71bfccad2794" />

## Colaborative Filtering model
The model based approached was used for this recommendation system, where algorithm such as BaselineOnly, SlopeOne and SVD
was experimented on. With SVD out performing the rest algorithms with an RMSE of 0.4097.

<img width="263" height="175" alt="image" src="https://github.com/user-attachments/assets/44283fca-cadc-402e-868e-1863df17bd78" />

# Dashboard
Here is a link to a User Friendly interface for Airbnb Price suggestion / recommender System:
https://predictiveperformanceanalysisofairbnbmetrics-ngqume5xlwkuulbkq.streamlit.app/ (Price)
https://predictiveperformanceanalysisofairbnbmetrics-8bysfmucc3l2hpevc.streamlit.app/ (Recommendation System)
