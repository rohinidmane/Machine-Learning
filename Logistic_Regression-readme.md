# 🩺 Diabetes Prediction using Logistic Regression

## 📌 Introduction

This project demonstrates the implementation of **Logistic Regression**, a supervised machine learning classification algorithm, to predict whether a person has diabetes based on medical and health-related information.

The model uses the Diabetes dataset and classifies individuals into two categories:
- **0** – Non-Diabetic
- **1** – Diabetic

## 📊 What This Project Does

- Loads the Diabetes dataset using Pandas.
- Selects medical features for model training.
- Separates input features and target variable.
- Splits the dataset into training and testing sets.
- Trains a Logistic Regression classification model.
- Predicts diabetes outcomes.
- Evaluates model performance using a confusion matrix and classification report.

## 🔄 Project Workflow

1. Import the required Python libraries.
2. Load the Diabetes dataset (`diabetes.csv`).
3. Explore the dataset columns.
4. Select independent and dependent variables.
5. Split the dataset into training and testing sets.
6. Create and train the Logistic Regression model.
7. Predict outcomes using test data.
8. Evaluate the model performance.

## 📁 Dataset Information

**Dataset Name:** `diabetes.csv`

The dataset contains medical information used to predict diabetes.

### Input Features (X)

| Feature | Description |
|---|---|
| `Pregnancies` | Number of times pregnant |
| `Glucose` | Glucose concentration |
| `BloodPressure` | Diastolic blood pressure |
| `SkinThickness` | Triceps skin fold thickness |
| `Insulin` | Two-hour serum insulin level |
| `BMI` | Body Mass Index |
| `DiabetesPedigreeFunction` | Diabetes pedigree function |
| `Age` | Age of the individual |

### Target Variable (y)

| Column    | Description                    |
|-----------|--------------------------------|
| `Outcome` | 0 = Non-Diabetic, 1 = Diabetic |

## 🧠 Key Concepts Covered

### 1. Logistic Regression

Logistic Regression is a supervised machine learning algorithm used for classification problems.

It predicts the probability of an observation belonging to a particular class.

### 2. Independent and Dependent Variables

- **X:** Contains eight input features used to make predictions.
- **y:** Contains the target variable (`Outcome`).

### 3. Train-Test Split

The dataset is divided into training and testing sets.

- Training data: 70%
- Testing data: 30%
- Random state: 42

### 4. Model Training

The Logistic Regression model is created using:

`LogisticRegression(max_iter=5000)`

The `max_iter` parameter specifies the maximum number of iterations allowed for the optimization algorithm to converge.

### 5. Model Evaluation

The model is evaluated using the following metrics:

| Metric            | Description                                                       |
|-------------------|-------------------------------------------------------------------|
| Accuracy Score    | Measures the overall proportion of correct predictions            |
| Confusion Matrix  | Shows correct and incorrect classification counts                 |
| Precision         | Measures how many positive predictions are actually positive      |
| Recall            | Measures how many actual positive cases are correctly identified  |
| F1-Score          | Harmonic mean of precision and recall                             |
| Support           | Number of actual observations in each class                       |

## 🛠️ Tech Stack

| Technology            | Purpose                                            |
|-----------------------|----------------------------------------------------|
| Python                | Programming language                               |
| Pandas                | Data loading and manipulation                      |
| Scikit-learn          | Machine learning implementation                    |
| Logistic Regression   | Classification algorithm                           |
| Train-Test Split      | Dividing data into training and testing sets       |
| Confusion Matrix      | Evaluating classification performance              |
| Classification Report | Displaying precision, recall, F1-score and support |
| Jupyter Notebook      | Writing and executing Python code                  |

## 📈 Operations Performed

| Function / Method             | Purpose                                       |
|-------------------------------|-----------------------------------------------|
| `pd.read_csv()`               | Loads the Diabetes dataset                    |
| `df.columns`                  | Displays column names                         |
| `df[['column1', 'column2']]`  | Selects specific input features               |
| `train_test_split()`          | Splits data into training and testing sets    |
| `LogisticRegression()`        | Creates the Logistic Regression model         |
| `fit()`                       | Trains the model                              |
| `predict()`                   | Predicts outcomes using test data             |
| `classification_report()`     | Generates classification performance metrics  |
| `confusion_matrix()`          | Displays the confusion matrix                 |

## 💡 Key Learnings

- Understanding supervised machine learning classification.
- Learning how Logistic Regression works.
- Selecting independent and dependent variables.
- Splitting a dataset into training and testing sets.
- Training a classification model using Scikit-learn.
- Making predictions on unseen test data.
- Evaluating model performance using a confusion matrix and classification report.

## 📁 Project Structure

```
Diabetes-Prediction-Logistic-Regression/
│
├── diabetes.csv
├── Logistic_Regression.ipynb
└── README.md
```

## 🚀 Future Improvements

- Perform Exploratory Data Analysis (EDA).
- Handle missing or invalid medical values.
- Apply feature scaling.
- Evaluate the model using accuracy, precision, recall and F1-score.
- Compare Logistic Regression with other classification algorithms.
- Tune model hyperparameters to improve performance.