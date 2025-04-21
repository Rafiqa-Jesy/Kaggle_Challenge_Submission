# Kaggle_Challenge_Submission
Submission Notebook and Summary for the Kaggle Challenge - Titanic Machine Learning from Disaster


# Project Overview : Titanic Machine Learning From Disaster
Objective:
The goal of this project was to predict survival on the Titanic based on various passenger features. I approached this challenge using several different machine learning models and various techniques such as feature engineering, hyperparameter tuning, and ensembling. 

1. Initial Exploration & Setup:
In the beginning, I imported necessary libraries such as pandas, numpy, seaborn, sklearn, and others for data processing, visualization, and model training. I then loaded the train and test datasets from the Kaggle Titanic dataset and performed an initial exploration, including:

-Checking for missing data

-Filling missing values in Age, Embarked, and Fare columns

-Dropping columns like Cabin due to a high percentage of missing values

2. Data Preprocessing & Feature Engineering:
I converted categorical variables (Sex, Embarked) into numeric format using Label Encoding.

Feature engineering was performed by extracting titles from the Name column and creating new features like:

FamilySize (sum of SibSp and Parch)

IsAlone (binary feature indicating if a passenger is traveling alone)

I also removed unneeded features like Name, Ticket, and PassengerId.

3. Initial Model: Random Forest Classifier
Initially, I trained a Random Forest Classifier on the processed dataset and used it to make predictions.

I achieved a moderate score but realized the model was potentially overfitting.

4. Tuning the Random Forest Model:
To improve performance, I used GridSearchCV to fine-tune hyperparameters such as:

n_estimators, max_depth, and min_samples_split

The tuned model provided better results.

5. Trying Other Models:
After working with Random Forest, I moved to other algorithms, trying XGBoost, LightGBM, and CatBoost, hoping they would outperform the Random Forest model on this structured dataset.

XGBoost didn’t provide substantial improvements and required fine-tuning, which led to high computation time.

I couldn't make it work with LIGHTGBM, so I stopped working with that in midway. I didn't submit that version, I started working with CatBoost instead.


Challenges Faced:
Missing Data Handling: Handling missing data was tricky, especially for the Cabin column, where dropping it seemed like the best option, though this led to the loss of valuable information.

Model Overfitting: Even with Random Forest, the model was prone to overfitting. I worked to address this by fine-tuning hyperparameters, but it still wasn’t perfect.

Feature Engineering: Extracting titles and creating new features like FamilySize and IsAlone required a lot of trial and error. Some features improved performance, but others didn’t make a significant impact.

Computational Efficiency: Models like XGBoost and LightGBM were computationally expensive and time-consuming, especially during hyperparameter tuning.

Summary of What Was Successful:
Data Preprocessing: Successfully handled missing data and converted categorical variables into usable features.

Feature Engineering: Created new, meaningful features like Title, FamilySize, and IsAlone.

What Didn’t Work:
XGBoost and LightGBM: While both are strong models, they didn’t significantly improve the performance. I couldn't complete the LightGBM version. 
