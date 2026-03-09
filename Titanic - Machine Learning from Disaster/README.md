Titanic Survival Prediction

This project predicts passenger survival on the Titanic using machine learning.

The goal is to analyze the dataset, perform feature engineering, train multiple models, and generate predictions for Kaggle submission.

Dataset

The dataset comes from the Kaggle Titanic competition.

Files used:

train.csv

test.csv

Main features include:

Passenger class

Sex

Age

Fare

Family relationships

Embarkation port

Project Workflow

The project follows a typical data science pipeline:

Data loading

Data inspection

Exploratory Data Analysis (EDA)

Feature engineering

Data preprocessing

Model training

Cross validation

Feature importance analysis

Model comparison

Ensemble prediction

Kaggle submission file generation

Exploratory Data Analysis

EDA revealed several important patterns:

Survival by Sex

Female passengers had a much higher survival rate than males.

Survival by Passenger Class

First-class passengers had a higher survival rate compared to second and third class.

Survival by Age

Children had a higher survival probability compared to adults.

Feature Engineering

Several new features were created to improve model performance.

FamilySize

FamilySize = SibSp + Parch + 1

This represents the total number of family members traveling together.

IsAlone

Passengers traveling alone may have different survival probabilities.

Title Extraction

Passenger titles were extracted from the Name column.

Examples:

Mr

Mrs

Miss

Master

These titles indirectly capture gender and age information.

Models Used

Two machine learning models were trained.

Random Forest

A tree-based ensemble model that performs well on structured tabular datasets.

LightGBM

A gradient boosting framework that is fast and highly effective for structured data problems.

Model Evaluation

Cross-validation was used to evaluate model performance.

Typical results:

RandomForest Accuracy ≈ 0.80
LightGBM Accuracy ≈ 0.82

Ensemble Method

Predictions from both models were combined using averaging.

Final prediction:

final_prediction = (rf_prediction + lgb_prediction) / 2

Ensembling improves robustness and performance.

Kaggle Submission

The final predictions are saved as:

submission.csv

Format:

PassengerId,Survived

This file can be directly submitted to Kaggle.

Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
LightGBM

Project Goal

This project demonstrates a full machine learning workflow including:

data analysis

feature engineering

model training

model evaluation

prediction generation

It serves as a portfolio project for data science and machine learning roles.
