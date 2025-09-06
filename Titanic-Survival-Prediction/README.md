Titanic Survival Prediction

Problem Statement

The Titanic disaster is one of the most infamous shipwrecks in history.
The goal of this project is to predict whether a passenger survived or not based on information such as age, sex, passenger class, and family relations.

This is a binary classification problem:

0 → Did not survive

1 → Survived



---

Dataset

Source: Kaggle Datasets

Files used:

train.csv → training data with labels (Survived)

test.csv → test data without labels



Important Features:

Pclass → Ticket class (1st, 2nd, 3rd)

Sex → Gender

Age → Passenger’s age

SibSp → # of siblings/spouses aboard

Parch → # of parents/children aboard

Fare → Ticket fare

Embarked → Port of embarkation



---

Approach

1. Data Preprocessing

Handled missing values (Age, Embarked, Fare).

Dropped irrelevant columns (PassengerId, Name, Ticket, Cabin).

Encoded categorical variables (Sex, Embarked).


2. Feature Engineering

Created new features to improve predictive power:

FamilySize = SibSp + Parch + 1

IsAlone = 1 if FamilySize==1 else 0

AgeGroup (child, young adult, adult, senior)

FareBand (low, medium, high, very high)



3. Model Building

Trained multiple models for comparison:

Logistic Regression

Random Forest Classifier


4. Evaluation

Used accuracy score to evaluate performance.

Random Forest achieved the best validation accuracy (~82%).



---

Results

Training Accuracy: ~98%

Validation Accuracy: ~78%


The model shows that gender, passenger class, and family status are the most important predictors of survival.
