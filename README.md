# Predictive_Performance_Analysis_of_Airbnb_Metrics
Dissertation
# Project Overview
The aim of this project is to predict an Airbnb price predictive model and to also buld a recommendation system
That would help property owners in looking to invest in the shortlet business via the Airbnb platform.
# Methodology
Our approach combined two methodologies—Regression Models and Collaborative Filtering
 
 ## Price Prediction Models
<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/1595d915-533c-451f-b5e1-f722436afdf8" />

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/62a8d680-b762-4700-a889-2d5af6774fae" />

## Train vs Test Performance
Key observations
1. Linear Regression

Train ≈ Test → Good generalisation, but underfitting

2. Decision Tree

Slight gap → Mild overfitting

3. Random Forest

Huge gap (0.144 vs 0.374) → Strong overfitting

4. XGBoost

Smaller gap than RF → Better regularisation

Although Random Forest achieved very low training error, the large gap indicates overfitting. XGBoost provides a better bias-variance trade-off. XGBoost was selected as the final model because it achieved the lowest RMSE, highest R², and demonstrated strong generalisation with minimal overfitting.

<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/42536a55-b91b-47a2-bca0-5e8930c0315c" />


Predictions closely follow the actual values, though slight deviations exist for high-priced listings

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/a8da2446-5590-4367-9925-8c1fea564b50" />


## Colaborative Filtering model
The model based approached was used for this recommendation system, where algorithm such as BaselineOnly, SlopeOne and SVD
was experimented on. With SVD out performing the rest algorithms with an RMSE of 0.4097.

<img width="1390" height="590" alt="image" src="https://github.com/user-attachments/assets/f96a0402-31ce-46ba-8d06-10f31e3aafe8" />

## Conclusion
This study demonstrates that ensemble learning methods, particularly XGBoost, significantly improve Airbnb price prediction accuracy, providing a reliable tool for pricing strategy and decision-making.

# Dashboard
Here is a link to a User Friendly interface for Airbnb Price suggestion / recommender System:
https://predictiveperformanceanalysisofairbnbmetrics-ngqume5xlwkuulbkq.streamlit.app/ (Price)
https://predictiveperformanceanalysisofairbnbmetrics-8bysfmucc3l2hpevc.streamlit.app/ (Recommendation System)
