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
https://colab.research.google.com/drive/1CWxsgGzSSbPbTedovPkWkYgH9udlfQs4#scrollTo=NIjFTQ_CRu0s (Analysis)


# Interactive Dashboard (Artefact)
Here is a link to a User Friendly interface for Airbnb Price suggestion / recommender System:
https://predictiveperformanceanalysisofairbnbmetrics-4asnlpyjsjc42588x.streamlit.app/ (Price)
https://predictiveperformanceanalysisofairbnbmetrics-8bysfmucc3l2hpevc.streamlit.app/ (Recommendation System)
