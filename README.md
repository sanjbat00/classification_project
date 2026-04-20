# classification_project

Website Classification using Machine Learning
 Overview

This project builds an end-to-end machine learning pipeline to classify websites into predefined categories based on structured features. The goal is to automate content categorization, which can be useful for search engines, recommendation systems, and content filtering.

 Key Features
 Exploratory Data Analysis (EDA) with insights
 Data preprocessing using pipelines
 Multiple classification models implemented:
Logistic Regression
Decision Tree
Random Forest
Support Vector Machine (SVM)
K-Nearest Neighbors (KNN)
 Hyperparameter tuning using GridSearchCV
 Model evaluation using Accuracy, Precision, Recall, and F1-score
 Model saving for reuse
 (Optional) Deployment using Streamlit
 Project Structure
website-classification-ml/
│
├── data/
│   └── website_classification.csv
│
├── notebooks/
│   └── EDA_and_Modeling.ipynb
│
├── src/
│   ├── preprocess.py
│   ├── train.py
│   ├── evaluate.py
│
├── models/
│   └── best_model.pkl
│
├── app/
│   └── app.py
│
├── requirements.txt
└── README.md
 Exploratory Data Analysis
Checked for missing values and handled appropriately
Analyzed feature distributions and correlations
Identified class imbalance in target variable
Visualized data using histograms, count plots, and heatmaps
 Data Preprocessing
Handled categorical variables using encoding techniques
Scaled numerical features using StandardScaler
Built a reusable preprocessing pipeline using ColumnTransformer
 Models Used

The following models were trained and evaluated:

Model	Description
Logistic Regression	Baseline linear model
Decision Tree	Rule-based model
Random Forest	Ensemble model for better accuracy
SVM	Effective for high-dimensional data
KNN	Distance-based classifier
 Hyperparameter Tuning
Used GridSearchCV to optimize model parameters
Performed cross-validation to ensure robustness
Selected best model based on F1-score
 Model Evaluation

Evaluation metrics used:

Accuracy
Precision
Recall
F1 Score

Example results:

Model	               Accuracy	            F1 Score
Random Forest	          91%                 .91
SVM	                    78%                  .77
Logistic Reg.	          60%                  .56


 Model Saving

The best-performing model is saved using joblib:



A simple web app is built using Streamlit for real-time predictions.



streamlit run app/app.py
