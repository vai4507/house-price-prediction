# house-price-prediction
This project predicts housing prices using the California Housing dataset. It includes data cleaning, EDA, log transformations, one-hot encoding, and feature engineering. Models like Linear Regression and Random Forest Regressor were trained, with Random Forest (tuned via GridSearchCV) delivering the best performance.

🏡 Housing Price Prediction
📌 Project Overview

This project predicts housing prices (median house value) using the California Housing dataset.
It applies data preprocessing, feature engineering, visualization, and machine learning models (Linear Regression & Random Forest) to build a predictive system.

⚙️ Tech Stack

Python 🐍

Libraries: numpy, pandas, matplotlib, seaborn, scikit-learn

Models: Linear Regression, Random Forest Regressor

📊 Workflow
1. Data Loading & Cleaning

Loaded dataset (housing.csv)

Removed missing values with dropna()

Checked data types and distributions

2. Exploratory Data Analysis (EDA)

Histograms of all features

Correlation heatmaps

Scatter plots (latitude vs longitude) → showed that houses near the ocean are more expensive

3. Feature Engineering

Log transformation for skewed features (total_rooms, total_bedrooms, population, households)

One-hot encoding for categorical feature ocean_proximity

Created new features:

train_data['bedroom_ratio'] = train_data['total_bedrooms'] / train_data['total_rooms']

train_data['household_ratio'] = train_data['total_rooms'] / train_data['households']

4. Model Training

Train-test split (75% / 25%)

Standardized features with StandardScaler

Baseline: Linear Regression

Advanced: Random Forest Regressor

6. Model Optimization

Tuned Random Forest hyperparameters using GridSearchCV

Best parameters selected and model re-trained

✅ Results

Linear Regression: baseline performance

Random Forest (optimized): significantly better predictive accuracy

Key Insight:

Houses closer to the ocean tend to have higher prices

Log-transformation & feature ratios improve model performance


