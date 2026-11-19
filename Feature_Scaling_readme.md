# 📏 Feature Scaling – Data Preprocessing

## 📌 Introduction
Feature Scaling is an important data preprocessing technique used in machine learning to bring numerical features into a similar range.

It prevents features with larger values from dominating those with smaller values. This project explores different feature scaling techniques using Scikit-learn and applies Min-Max Scaling to the Diabetes dataset for K-Nearest Neighbors (KNN) classification.

## 📊 What This Project Does
- Creates a sample Salary dataset using Pandas.
- Applies different feature scaling techniques.
- Compares Min-Max, Standard, MaxAbs, and Robust Scaling.
- Loads the Diabetes dataset from a CSV file.
- Applies Min-Max Scaling to numerical features.
- Splits the dataset into training and testing sets.
- Builds a KNN classification model.
- Evaluates predictions using a classification report.

## 🔄 Feature Scaling Workflow

Load Dataset  
    ↓  
Identify Numerical Features  
    ↓  
Apply Feature Scaling  
    ↓  
Split Data into Training and Testing Sets  
    ↓  
Initialize KNN Classifier  
    ↓  
Train the Model  
    ↓  
Make Predictions  
    ↓  
Evaluate Model Performance

## 📊 Dataset Information

This project uses two datasets:

### 1. Salary Dataset
A manually created dataset containing salary values.

**Initial Salary Values:**
- 70,000
- 65,000
- 52,000
- 45,000

An additional salary value of 2,000,000 is added to demonstrate the effect of outliers on Robust Scaling.

### 2. Diabetes Dataset
**File Name:** `diabetes.csv`

The dataset contains medical features used for diabetes classification.

**Features:**
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

**Target Variable:** `Outcome`

## 🧠 Key Concepts Covered

### 1. Min-Max Scaling
- Transforms values into a specified range, usually 0 to 1.
- Uses minimum and maximum values to scale the data.
- Sensitive to outliers.

### 2. Standard Scaling
- Transforms data based on mean and standard deviation.
- Produces values with a mean of approximately 0 and standard deviation of 1.
- Does not restrict values to a fixed range.

### 3. MaxAbs Scaling
- Divides each value by the maximum absolute value of its feature.
- Scales values into the range -1 to 1.
- Preserves zero values and is useful for sparse data.

### 4. Robust Scaling
- Uses the median and interquartile range (IQR).
- Reduces the influence of outliers.
- Useful for datasets containing extreme values.

### 5. K-Nearest Neighbors (KNN)
- A supervised machine learning algorithm.
- Classifies data based on the nearest data points.
- Feature scaling is important because KNN uses distance calculations.

## 🛠️ Tech Stack

- Python
- Pandas
- Scikit-learn

## 📈 Operations Performed

| Operation                 | Description                                              |
|---------------------------|----------------------------------------------------------|
| `pd.DataFrame()`          | Creates a DataFrame for salary values.                   |
| `MinMaxScaler()`          | Scales features into a specified range.                  |
| `StandardScaler()`        | Standardizes features using mean and standard deviation. |
| `MaxAbsScaler()`          | Scales features using maximum absolute values.           |
| `RobustScaler()`          | Scales features using median and IQR.                    |
| `pd.read_csv()`           | Loads the Diabetes dataset.                              |
| `df.columns`              | Displays dataset column names.                           |
| `fit_transform()`         | Learns scaling parameters and transforms data.           |
| `train_test_split()`      | Splits data into training and testing sets.              |
| `KNeighborsClassifier()`  | Initializes the KNN classification model.                |
| `fit()`                   | Trains the classification model.                         |
| `predict()`               | Predicts the target values.                              |
| `classification_report()` | Displays precision, recall, F1-score, and support.       |

## 💡 Key Learnings

1. Understood the importance of Feature Scaling in machine learning.
2. Learned different scaling techniques and their applications.
3. Understood how outliers affect scaling methods.
4. Learned why Robust Scaling is useful for datasets containing extreme values.
5. Practiced applying Min-Max Scaling to a real-world dataset.
6. Understood why feature scaling is important for distance-based algorithms like KNN.
7. Practiced building and evaluating a KNN classification model.

## 📁 Project Structure

```
Feature-Scaling/
│
├── Feature_Scaling.ipynb
├── diabetes.csv
└── README.md
```

## 🚀 Future Improvements

- Compare the results of different scaling techniques.
- Apply Standard, Robust, and MaxAbs Scaling to the Diabetes dataset.
- Experiment with different K values in KNN.
- Compare KNN performance before and after feature scaling.
- Use a Pipeline to prevent data leakage during preprocessing.
- Explore other feature preprocessing techniques.
