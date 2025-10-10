# Netflix Customer Churn Prediction
## 1. Project Overview
This project aims to predict customer churn for a Netflix-like subscription service. By analyzing customer behavior and demographic data, we build and evaluate several machine learning models to identify customers who are at a high risk of canceling their subscriptions. The ultimate goal is to provide actionable insights that can help in developing targeted retention strategies.

## 2. Dataset
The analysis is based on the netflix_customer_churn (1).csv dataset, which contains 5,000 records and 14 features, including:

Customer Demographics: age, gender, region

Subscription Details: subscription_type, monthly_fee

Usage & Engagement Metrics: watch_hours, last_login_days, avg_watch_time_per_day

Account Information: device, payment_method, number_of_profiles, favorite_genre

Target Variable: churned (1 for churned, 0 for retained)

## 3. Project Workflow
The project is structured into the following key stages:

Exploratory Data Analysis (EDA): Investigating the dataset to uncover initial patterns, trends, and relationships between features and churn.

Feature Engineering: Creating new, more predictive features from existing data, such as an engagement_score.

Data Preprocessing: Cleaning the data, handling outliers, and encoding categorical variables to prepare them for modeling.

Model Building: Training several classification models to predict churn, including:

### Logistic Regression (Baseline)

### Decision Tree

### Random Forest

Model Evaluation: Assessing the performance of each model using metrics like accuracy, precision, recall, and the confusion matrix.

## 4. Key Findings from EDA
The initial analysis revealed several important insights:

The dataset is well-balanced, with a churn rate of approximately 50.3%.

Engagement metrics are strong predictors of churn. Customers who churned tend to have lower watch hours and more days since their last login.

The engagement_score feature, engineered from watch_hours and last_login_days, shows a clear separation between churned and retained customers.

There are significant outliers in watch_hours and avg_watch_time_per_day, which were handled using capping at the 99th percentile.

## 5. Setup and Installation
To run this project on your local machine, it is highly recommended to use a virtual environment to avoid library conflicts.

Environment Setup (for macOS):

Open your terminal and navigate to the project directory.

cd /path/to/your/project/folder

Create a virtual environment:

python3 -m venv churn_env

Activate the environment:

source churn_env/bin/activate

Install the required libraries:

pip install pandas scikit-learn seaborn matplotlib xgboost

## 6. How to Run the Models
With the virtual environment activated, you can run the model-building scripts directly from the terminal.

To run the Logistic Regression model:

python3 churn_model_logistic.py

To run the Decision Tree model:

python3 churn_model_decision_tree.py

To run the Random Forest model:

python3 churn_model_random_forest.py

To run the XGBoost model:

python3 churn_model_xgboost.py

Each script will preprocess the data, train the respective model, and print the accuracy, classification report, and confusion matrix as output. It will also save a plot of the confusion matrix as a .png file.

## 7. Expected Results
The models are expected to perform well due to the balanced dataset and effective feature engineering.

Logistic Regression (Baseline): Expected accuracy ~85%

Decision Tree, Random Forest, XGBoost: Expected to achieve similar or higher accuracy.

## 8. Author
Manmeet Kaur