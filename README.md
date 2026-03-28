# Predictive_Performance_Analysis_of_Airbnb_Metrics
Dissertation
# Project Overview
The aim of this project is to predict an Airbnb price predictive model and to also buld a recommendation system
That would help property owners in looking to invest in the shortlet business via the Airbnb platform.
# Methodology

## Correlation Heatmap

<img width="1989" height="1418" alt="image" src="https://github.com/user-attachments/assets/c922a9dc-1f35-4e89-94f1-137b44e507d9" />

## Sentiment Analysis
<img width="868" height="547" alt="image" src="https://github.com/user-attachments/assets/7d60228e-2b8f-4086-8010-e18325d8cc80" />

Our approach combined two methodologies
Regression Models and Collaborative Filtering
 
 ## Price Prediction Models
<img width="1389" height="589" alt="image" src="https://github.com/user-attachments/assets/2ab27a2f-1985-4231-9467-34b74874fb17" />

<img width="1390" height="590" alt="image" src="https://github.com/user-attachments/assets/2076f988-4861-47d8-aaa5-ea3d13e92356" />


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
Both BaselineOnly and SVD has almost similar RMSE and MAE, but BaselineOnly had shorter computation time. In Data science if the benchmark model and complex model have similar result, it is best to choose the baseline model and in this case it is the BaselineOnly. This models was trained using compound_scores with a rating scale of (-1, 1). The result shows that BaselineOnly performs better than the rest algorithm. Even though SVD has also most similar results with BaselineOne, it has a longer computational time and  in data science, if the baseline model performs better than the complex model, it is adviced to choose the basline model. The main reason is Occam’s Razor: the simplest solution is usually the best and Complex models are prone to overfitting, meaning they "memorise" noise in the training data and fail when they see new, real-world data, Simple models are easier to debug, faster to retrain, and cheaper to run in production, It is much easier to explain why a baseline model made a specific decision to stakeholders or regulators.

<img width="1389" height="589" alt="image" src="https://github.com/user-attachments/assets/542ce379-80d1-4ea8-9dab-31e2f2384fdf" />


## Conclusion
This study demonstrates that ensemble learning methods, particularly XGBoost, significantly improve Airbnb price prediction accuracy, providing a reliable tool for pricing strategy and decision-making. One of the major limitation is that the model pocesses the inability to address new listings aand guest which means it has a cold start problem and finally the model is biased due to the skewness of the sentiment scores.

# Dashboard
Here is a link to a User Friendly interface for Airbnb Price suggestion / recommender System:
https://predictiveperformanceanalysisofairbnbmetrics-4asnlpyjsjc42588x.streamlit.app/ (Price)
https://predictiveperformanceanalysisofairbnbmetrics-8bysfmucc3l2hpevc.streamlit.app/ (Recommendation System)
