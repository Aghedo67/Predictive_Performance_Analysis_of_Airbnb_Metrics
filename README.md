# 📊 Predictive Performance Analysis of Airbnb Metrics
## 📌 Project Overview

This project presents a unified analytical framework that integrates price prediction and recommendation systems to enhance decision-making for both Airbnb hosts and guests.

Unlike previous research that treats these problems separately, this study combines them to improve the overall marketplace experience, focusing on the Dublin Airbnb market.

## ❗ Project Rationale
- 🔍 Problem

Hosts rely heavily on intuition and social learning, lacking advanced pricing tools.

Guests face information overload, making it difficult to assess listing quality and choose optimal options.

- 💡 Solution

### Predictive Modelling
Generates actionable price predictions to help hosts optimize revenue.

### Recommender System
Provides personalized listing suggestions to simplify guest decision-making.

- 🎯 Goal

To develop a holistic system that integrates pricing intelligence with recommendation capabilities for improved marketplace efficiency.

## 🎯 Project Objectives

- Develop a predictive model to estimate optimal listing prices and identify key influencing features.

- Analyze guest reviews and sentiment to understand performance trends.

- Implement collaborative filtering techniques for personalized recommendations.

- Integrate outputs into an interactive analytical tool.

## 📂 Data Description
- 📌 Source

Inside Airbnb – a mission-driven platform providing open-access Airbnb data.

- 🌍 Context

Focus on Dublin, chosen for its:

High tourism density

Complex housing and rental dynamics

- 📊 Dataset Overview
1. Listings Dataset (listings.csv)

Contains detailed property-level information.

Key Features:

Price

Location (latitude & longitude)

Property type & room type

Host characteristics

Review scores

2. Reviews Dataset (reviews.csv)

Contains historical guest feedback.

Key Features:

Reviewer ID

Review date

Comment text

## 🔍 Exploratory Data Analysis (EDA)
- 😊 Guest Sentiment

Strong skew towards positive sentiment

Very low proportion of negative reviews

- 📈 Statistical Insights

Property size and capacity are key drivers of price

Sentiment and ratings show weak correlation with price

Most predictors are statistically significant (p < 0.05)

Bathrooms found to be not statistically significant (p = 0.476)

Overall model shows strong explanatory power (high F-statistic)

## 🤖 Models & Evaluation
- 1️⃣ Price Prediction Models

Linear Regression

Decision Tree

Random Forest

XGBoost

Evaluation Metrics:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score

- 2️⃣ Recommendation System Models

BaselineOnly

SlopeOne

Singular Value Decomposition (SVD)

Evaluation Approach:

5-fold cross-validation

Metrics:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

## 📊 Results
- 1️⃣ Price Prediction – XGBoost (Best Performing Model)

The XGBoost model achieved the strongest performance among all regression models, demonstrating strong generalisation and predictive accuracy.

- 📈 Model Performance (Log-Scaled Target):

Train RMSE: 0.2771

Test RMSE: 0.3910

Train MAE: 0.2080

Test MAE: 0.2665

R² Score: 0.6925

- 🔁 Cross-Validation Performance:

CV RMSE: 0.3784

CV MAE: 0.2721

CV R² Score: 0.6918

## 📌 Interpretation:

The small gap between training and testing errors indicates good generalisation with minimal overfitting.

The model explains approximately 69% of price variability.

Consistent cross-validation results confirm robustness and stability.

## 2️⃣ Collaborative Filtering – BaselineOnly

The BaselineOnly algorithm was evaluated using 5-fold cross-validation.

- 📊 Cross-Validation Results:

Metric	Fold 1	Fold 2	Fold 3	Fold 4	Fold 5	Mean	Std
RMSE	0.4228	0.4196	0.4237	0.4288	0.4243	0.4238	0.0030
MAE	0.3102	0.3080	0.3100	0.3123	0.3101	0.3101	0.0014

- ⏱️ Computational Performance:

Average Fit Time: 4.68 seconds

Average Test Time: 0.58 seconds

- 📌 Interpretation:

Low standard deviation indicates high consistency across folds.

Provides a reliable baseline for comparison with advanced models (e.g., SVD).

## 📊 Feature Engineering
- 🔑 Predictors for Price Model

host_response_rate

host_is_superhost

host_listings_count

accommodates

bedrooms

beds

maximum_nights

review_scores_rating

review_scores_cleanliness

review_scores_location

number_of_reviews

neighbourhood_freq

property_type_freq

- 🔑 Predictors for Recommendation System

reviewer_id

listing_id (id_x)

sentiment compound score (-1 to 1)

## 🧠 Methodology

Data Cleaning & Preprocessing

Handling missing values

Feature aggregation

Encoding categorical variables

Sentiment Analysis

Extract sentiment scores from review text

Generate compound sentiment scores

Model Development

Train and evaluate multiple models

Hyperparameter tuning

Performance validation

Recommendation System

Build collaborative filtering models

Evaluate using cross-validation

Integration

Combine predictive and recommendation outputs

Deploy via interactive interface

## 🖥️ Interactive Application

The project includes an interactive tool that:

Predicts listing prices

Visualizes price distributions

Provides personalized recommendations

## 🚀 Key Contributions

Integration of price prediction and recommendation systems

Application of sentiment analysis to Airbnb reviews

Development of a decision-support tool for hosts and guests

## ⚠️ Limitations

Sentiment data is heavily skewed toward positive reviews

Dataset limited to Dublin (may affect generalizability)

Cold-start problem in recommendation systems

## 🔮 Future Work

Implement deep learning approaches (e.g., neural collaborative filtering)

Expand analysis to multiple cities

Incorporate real-time dynamic pricing

Develop hybrid recommendation systems

## 🛠️ Tech Stack

Python (Pandas, NumPy, Scikit-learn)

XGBoost

Surprise Library

NLP (Sentiment Analysis)

Streamlit







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

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/bd884631-793a-4af2-9c3c-5c7d3c12a351" />



Predictions closely follow the actual values, though slight deviations exist for high-priced listings

<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/586d541b-7c65-4279-866f-ffccdb17dfbb" />


## Colaborative Filtering model
Both BaselineOnly and SVD has almost similar RMSE and MAE, but BaselineOnly had shorter computation time. In Data science if the benchmark model and complex model have similar result, it is best to choose the baseline model and in this case it is the BaselineOnly. This models was trained using compound_scores with a rating scale of (-1, 1). The result shows that BaselineOnly performs better than the rest algorithm. Even though SVD has also most similar results with BaselineOne, it has a longer computational time and  in data science, if the baseline model performs better than the complex model, it is adviced to choose the basline model. The main reason is Occam’s Razor: the simplest solution is usually the best and Complex models are prone to overfitting, meaning they "memorise" noise in the training data and fail when they see new, real-world data, Simple models are easier to debug, faster to retrain, and cheaper to run in production, It is much easier to explain why a baseline model made a specific decision to stakeholders or regulators.

<img width="1389" height="589" alt="image" src="https://github.com/user-attachments/assets/542ce379-80d1-4ea8-9dab-31e2f2384fdf" />


## Conclusion
This study demonstrates that ensemble learning methods, particularly XGBoost, significantly improve Airbnb price prediction accuracy, providing a reliable tool for pricing strategy and decision-making. One of the major limitation is that the model pocesses the inability to address new listings aand guest which means it has a cold start problem and finally the model is biased due to the skewness of the sentiment scores.

# Dashboard
Here is a link to a User Friendly interface for Airbnb Price suggestion / recommender System:
https://predictiveperformanceanalysisofairbnbmetrics-4asnlpyjsjc42588x.streamlit.app/ (Price)
https://predictiveperformanceanalysisofairbnbmetrics-8bysfmucc3l2hpevc.streamlit.app/ (Recommendation System)
