# 🏥 Health Insurance Cost Prediction – Linear & Multiple Linear Regression

## 📌 Introduction
Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values by identifying relationships between independent and dependent variables.

This project uses a Health Insurance dataset to explore data cleaning, exploratory data analysis (EDA), categorical encoding, correlation analysis, Simple Linear Regression, and Multiple Linear Regression.

The main objective is to understand how factors such as smoking status, age, and BMI are related to medical insurance costs.

## 📊 What This Project Does
- Loads the Health Insurance dataset using Pandas.
- Explores dataset information and statistical summaries.
- Identifies and removes duplicate records.
- Performs Exploratory Data Analysis (EDA).
- Visualizes numerical and categorical features.
- Converts binary categorical values into numerical values.
- Applies One-Hot Encoding to the region column.
- Performs correlation analysis using a heatmap.
- Builds a Simple Linear Regression model using smoker status.
- Builds a Multiple Linear Regression model using age, BMI, and smoker status.
- Evaluates model performance using R² Score.
- Visualizes the regression line and residual plot.
- Predicts medical costs for new input records.

## 🔄 Project Workflow

Load Health Insurance Dataset  
            ↓  
Explore Dataset Information  
            ↓  
Check and Remove Duplicates  
            ↓  
Perform Exploratory Data Analysis  
            ↓  
Visualize Numerical and Categorical Features  
            ↓  
Encode Categorical Variables  
            ↓  
Perform Correlation Analysis  
            ↓  
Build Simple Linear Regression Model  
            ↓  
Evaluate Model Performance  
            ↓  
Visualize Regression Line and Residuals  
            ↓  
Build Multiple Linear Regression Model  
            ↓  
Predict Medical Insurance Costs

## 📊 Dataset Information

**Dataset:** Health Insurance Dataset

**File Name:** `health_insurance.csv`

The dataset contains information about individuals and their medical insurance costs.

**Features explored include:**
- `age` – Age of the individual.
- `gender` – Gender of the individual.
- `bmi` – Body Mass Index.
- `smoker` – Smoking status.
- `region` – Residential region.
- `medical_cost` – Medical insurance cost.

**Target Variable:** `medical_cost`

**Independent Variables:**

Simple Linear Regression:
- `smoker`

Multiple Linear Regression:
- `age`
- `bmi`
- `smoker`

**Data Splitting:**
- Training Data: 80%
- Testing Data: 20%
- Random State: 42

## 🧠 Key Concepts Covered

### 1. Exploratory Data Analysis (EDA)
EDA is used to understand the dataset, identify patterns, and examine data distributions.

Operations performed:
- Dataset information using `df.info()`.
- Duplicate checking and removal.
- Statistical summary using `df.describe()`.
- Dataset shape and column information.
- Histograms, boxplots, and countplots.

### 2. Data Cleaning
- Identified duplicate records using `duplicated()`.
- Removed duplicate records using `drop_duplicates()`.
- Checked dataset dimensions after cleaning.

### 3. Categorical Encoding

**Label Encoding / Manual Binary Encoding:**
- Gender: Female = 0, Male = 1.
- Smoker: Non-smoker = 0, Smoker = 1.

**One-Hot Encoding:**
- Converted the categorical `region` column into separate binary columns using `pd.get_dummies()`.

### 4. Correlation Analysis
- Used correlation to understand relationships between numerical features.
- Created a correlation heatmap using Seaborn.
- Used correlation values to explore relationships between features and medical costs.

### 5. Simple Linear Regression
Simple Linear Regression uses one independent variable to predict a dependent variable.

**In this project:**
- Independent Variable (X): `smoker`
- Dependent Variable (Y): `medical_cost`

The model compares the average medical costs of smokers and non-smokers.

### 6. Multiple Linear Regression
Multiple Linear Regression uses two or more independent variables to predict a dependent variable.

**In this project:**
- Independent Variables: `age`, `bmi`, `smoker`
- Dependent Variable: `medical_cost`

It helps understand how multiple factors together relate to medical insurance costs.

### 7. Regression Line
A regression line is the best-fit line that represents the average relationship between independent and dependent variables.

In the smoker-based regression:
- Smoker = 0 represents non-smokers.
- Smoker = 1 represents smokers.
- The difference between the two predicted values represents the estimated average medical cost difference between the groups.

### 8. Residual Plot
A residual is the difference between the actual value and the predicted value.

**Formula:**

Residual = Actual Value − Predicted Value

Interpretation:
- Points above zero: Model underestimated the cost.
- Points below zero: Model overestimated the cost.
- Points close to zero: Predictions are more accurate.

The residual plot helps identify unexplained variation and assess regression model assumptions.

### 9. R² Score
R² Score measures how much of the variation in the target variable is explained by the regression model.

- R² closer to 1 indicates a better fit.
- R² around 0 indicates limited explanatory power.
- A negative R² indicates performance worse than predicting the mean of the actual values.

## 🛠️ Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## 📈 Operations Performed

| Operation             | Description                                             |
|-----------------------|---------------------------------------------------------|
| `pd.read_csv()`       | Loads the Health Insurance dataset.                     |
| `df.info()`           | Displays dataset information.                           |
| `df.duplicated()`     | Identifies duplicate records.                           |
| `df.drop_duplicates()`| Removes duplicate records.                              |
| `df.shape`            | Returns the number of rows and columns.                 |
| `df.describe()`       | Generates statistical summaries.                        |
| `sns.histplot()`      | Visualizes numerical data distributions.                |
| `sns.boxplot()`       | Identifies data spread and potential outliers.          |
| `sns.countplot()`     | Visualizes categorical data frequencies.                |
| `df.loc[]`            | Updates categorical values.                             |
| `pd.get_dummies()`    | Performs One-Hot Encoding.                              |
| `df.corr()`           | Calculates correlations between numerical columns.      |
| `sns.heatmap()`       | Visualizes the correlation matrix.                      |
| `train_test_split()`  | Splits data into training and testing sets.             |
| `LinearRegression()`  | Initializes the Linear Regression model.                |
| `fit()`               | Trains the regression model.                            |
| `predict()`           | Predicts medical costs.                                 |
| `r2_score()`          | Evaluates regression performance.                       |
| `plt.scatter()`       | Creates scatter plots.                                  |
| `plt.plot()`          | Displays the regression line.                           |
| `plt.axhline()`       | Draws a horizontal reference line in the residual plot. |

## 💡 Key Learnings

1. Learned how to perform Exploratory Data Analysis on a real-world dataset.
2. Practiced identifying and removing duplicate records.
3. Understood how to visualize numerical and categorical features.
4. Learned binary encoding and One-Hot Encoding.
5. Understood how to perform correlation analysis using a heatmap.
6. Learned the difference between Simple and Multiple Linear Regression.
7. Practiced predicting medical costs using Linear Regression.
8. Understood how to interpret regression lines and residual plots.
9. Learned how to evaluate regression models using R² Score.
10. Understood how age, BMI, and smoking status can be explored as factors related to medical insurance costs.

## 📁 Project Structure

```
Health-Insurance-Cost-Prediction/
│
├── Health_Insurance.ipynb
├── health_insurance.csv
└── README.md
```

## 🚀 Future Improvements

- Include additional features such as gender and region in the prediction model.
- Compare Simple and Multiple Linear Regression performance.
- Evaluate models using MAE, MSE, and RMSE.
- Explore feature selection techniques.
- Check regression assumptions and multicollinearity.
- Experiment with Ridge and Lasso Regression.
- Compare Linear Regression with other regression algorithms.
- Improve prediction performance through feature engineering.