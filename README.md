# Titanic Survival Prediction

## Overview
This project uses machine learning algorithms to predict the survival of passengers on the Titanic based on various features such as age, sex, class, and more.

## Dataset
- **Source**: Kaggle Titanic dataset
- **Number of passengers**: 891
- **Features**: Survival status, age, sex, class, and more

## Preprocessing
- Dropped unnecessary columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Filled missing values in `Embarked` column with the most frequent value
- Used `KNNImputer` to impute missing values in `Age` column
- One-hot encoded categorical variables: `Sex`, `Embarked`
- Scaled numerical variables using `StandardScaler`

## Models

### Logistic Regression
- **Accuracy score**: 0.8101

### Random Forest Classifier
- **Number of estimators**: 1000
- **Accuracy score**: 0.8101

### XGBoost Classifier
- **Accuracy score**: 0.8045

## Results
| Model                    | Accuracy Score |
|--------------------------|----------------|
| Logistic Regression      | 0.8101         |
| Random Forest Classifier | 0.8101         |
| XGBoost Classifier       | 0.8045         |

## Conclusion
The Random Forest Classifier and Logistic Regression models performed equally well, achieving an accuracy score of 0.8101. The XGBoost Classifier performed slightly worse, with an accuracy score of 0.8045.


