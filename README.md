# Titanic Survival Prediction

This repository contains a machine learning project focused on predicting the survival of passengers aboard the Titanic. The project leverages various data preprocessing techniques, feature engineering, and model selection methodologies to achieve optimal performance.

<img width="717" alt="image" src="https://github.com/user-attachments/assets/8d0a5ec9-5f75-436f-9e38-52afea7df3b5">

## Project Overview

The Titanic dataset is one of the most well-known datasets used in data science and machine learning. It contains data on passengers such as their age, gender, class, fare, and more. The goal of this project is to build a model that can predict whether a passenger survived or not based on these features.

## Dataset

The dataset used in this project is sourced from Kaggle's Titanic dataset. It contains 12 columns and 891 rows, with some missing values that were handled during preprocessing.

- **Survived**: Outcome variable (0 = No, 1 = Yes)
- **Pclass**: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Fare**: Ticket fare
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

  <img width="832" alt="image" src="https://github.com/user-attachments/assets/9c3ea93c-0cca-4bf5-97f2-95a74f86ea14">

  ![Pairplots](https://github.com/user-attachments/assets/756deaf4-11c0-4633-9353-198b0ee079a9)


## Preprocessing

1. **Handling Missing Data**:
   - Imputed missing values in the "Age" column using KNN Imputer.
   - Filled missing values in the "Embarked" column with the mode.

     <img width="421" alt="image" src="https://github.com/user-attachments/assets/db65adab-337b-4278-ae60-382607cbb0c7">


2. **Feature Selection**:
   - Dropped less significant features: `PassengerId`, `Name`, `Ticket`, and `Cabin`.

   <img width="385" alt="image" src="https://github.com/user-attachments/assets/7c98d124-ea38-466b-824b-c09bb5e4ae1e">

3. **Encoding Categorical Variables**:
   - Applied One-Hot Encoding to the `Sex` and `Embarked` columns.
     
     <img width="594" alt="image" src="https://github.com/user-attachments/assets/c3581f9e-af08-44f3-a238-2005a4d76859">


4. **Data Scaling**:
   - Standardized the features using `StandardScaler` to ensure all features contribute equally to the model.
     
     <img width="424" alt="image" src="https://github.com/user-attachments/assets/8a220be8-b941-49e9-96c9-fcafda66d500">


## Model Building

![Correlation heatmap](https://github.com/user-attachments/assets/b764e2a9-7434-46f3-826f-f6f841f0fb50)


Multiple models were built and evaluated to predict survival:

- **Logistic Regression**: A baseline model with an accuracy of 0.76.
- **Random Forest Classifier**: Achieved an accuracy of 0.79.
- **XGBRFClassifier**: Another ensemble model, which was also tested for performance.

## Hyperparameter Tuning

GridSearchCV was applied to the Random Forest model to find the best combination of hyperparameters. The best parameters identified were:

- **n_estimators**: 100
- **max_depth**: 30
- **min_samples_split**: 5
- **min_samples_leaf**: 2
- **bootstrap**: True

This optimized model achieved a cross-validated accuracy score of 0.85.

## Results

- The best model achieved an accuracy of 0.85 on the cross-validation set, demonstrating a strong predictive capability on the Titanic dataset.

## Conclusion

This project showcases the end-to-end process of building a machine learning model, from data preprocessing to model optimization. The Random Forest model with tuned hyperparameters provided the best performance in predicting passenger survival.

## Future Work

- Explore other advanced models and ensemble techniques.
- Further improve model accuracy with more feature engineering and cross-validation strategies.
- Deploy the model as a web application for interactive predictions.

## Acknowledgments

This project was inspired by the Titanic dataset on Kaggle, a great resource for learning data science and machine learning.
