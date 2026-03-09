# 🚢 Titanic Survival Prediction
Machine Learning | Data Science | Kaggle

# 🚢 Titanic Survival Prediction

A machine learning project that predicts whether a passenger survived the Titanic disaster using structured tabular data.

This project demonstrates a full **data science workflow**, including exploratory data analysis, feature engineering, model training, evaluation, and Kaggle submission generation.

---

# 📊 Dataset

The dataset comes from the Kaggle competition:

**Titanic - Machine Learning from Disaster**

It contains passenger information such as:

* Passenger class
* Name
* Sex
* Age
* Fare
* Family relationships
* Embarkation port

Files used in this project:

```
train.csv
test.csv
```

---

# 📁 Project Structure

```
titanic-survival-prediction
│
├── data
│   ├── train.csv
│   └── test.csv
│
├── notebook
│   └── titanic_full_ds_project.ipynb
│
├── submission
│   └── submission.csv
│
├── README.md
└── requirements.txt
```

---

# 🔎 Project Workflow

This project follows a standard **data science pipeline**.

1. Data Loading
2. Data Inspection
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Data Preprocessing
6. Model Training
7. Cross Validation
8. Feature Importance Analysis
9. Model Comparison
10. Ensemble Prediction
11. Kaggle Submission File Generation

---

# 📈 Exploratory Data Analysis (EDA)

EDA was performed to identify patterns related to passenger survival.

### Survival by Sex

Female passengers had a significantly higher survival rate compared to male passengers.

### Survival by Passenger Class

Passengers in **first class** had the highest survival rate, while **third class** passengers had the lowest.

### Survival by Age

Younger passengers tended to have a higher survival probability.

These insights guided the feature engineering process.

---

# 🧠 Feature Engineering

To improve model performance, several new features were created.

### FamilySize

```
FamilySize = SibSp + Parch + 1
```

This represents the total number of family members traveling together.

---

### IsAlone

Passengers traveling alone may have different survival probabilities.

```
IsAlone = FamilySize == 1
```

---

### Title Extraction

Passenger titles were extracted from the **Name** column.

Examples:

```
Mr
Mrs
Miss
Master
```

These titles indirectly encode **gender and age information**.

---

# 🤖 Machine Learning Models

Two machine learning models were trained and evaluated.

## Random Forest

Random Forest is an ensemble learning method based on decision trees.

Advantages:

* Handles tabular data well
* Robust to overfitting
* Easy to interpret feature importance

---

## LightGBM

LightGBM is a gradient boosting framework optimized for performance and speed.

Advantages:

* Fast training speed
* High predictive performance
* Effective for structured datasets

---

# 📊 Model Evaluation

Models were evaluated using **cross-validation**.

Typical results:

```
RandomForest Accuracy ≈ 0.80
LightGBM Accuracy ≈ 0.82
```

LightGBM generally produced slightly better results.

---

# 🔗 Ensemble Method

To improve prediction robustness, predictions from both models were combined.

```
final_prediction = (rf_prediction + lgb_prediction) / 2
```

Ensembling helps reduce model variance and improve overall performance.

---

# 🏆 Kaggle Submission

Final predictions are saved as:

```
submission.csv
```

Format:

```
PassengerId,Survived
892,0
893,1
894,0
```

This file can be directly submitted to the Kaggle competition.

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* LightGBM

---

# 🎯 Project Objective

The goal of this project is to demonstrate an **end-to-end machine learning workflow**, including:

* data exploration
* feature engineering
* model training
* model evaluation
* prediction generation

This project serves as a **portfolio example for data science and machine learning roles**.
