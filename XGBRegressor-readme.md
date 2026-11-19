# 🏡 XGBoost Regression – California Housing Price Prediction

This project demonstrates **XGBoost (Extreme Gradient Boosting)**, an advanced ensemble machine learning algorithm, to predict California housing prices using the California Housing dataset.

The project covers dataset loading, train-test splitting, feature scaling, model training, prediction, evaluation, feature importance visualization, model saving, and predicting prices for new house data.

## 📊 What This Project Does

- Loads the California Housing dataset.
- Separates input features and target values.
- Splits the dataset into training and testing sets.
- Applies feature scaling using StandardScaler.
- Trains an XGBoost Regressor model.
- Predicts house prices using the trained model.
- Evaluates model performance using RMSE and R² Score.
- Visualizes feature importance.
- Compares actual and predicted house prices.
- Saves the trained model and scaler using Joblib.
- Predicts the price of a new custom house.

## 🔄 Machine Learning Workflow

Load California Housing Dataset  
            ⬇  
Separate Features (X) and Target (y)  
            ⬇  
Train-Test Split (80% Training, 20% Testing)  
            ⬇  
Feature Scaling using StandardScaler  
            ⬇  
Initialize XGBoost Regressor  
            ⬇  
Train the Model using `fit()`  
            ⬇  
Make Predictions using `predict()`  
            ⬇  
Evaluate Model Performance  
            ⬇  
Visualize Feature Importance  
            ⬇  
Compare Actual vs Predicted Values  
            ⬇  
Save Model and Scaler using Joblib  
            ⬇  
Predict Price for New House Data

## 📊 Dataset Information

**Dataset:** California Housing Dataset

**Source:** Scikit-learn built-in dataset using `fetch_california_housing()`.

- **Total Records:** 20,640
- **Total Features:** 8
- **Target Variable:** Median House Value

### Input Features

1. `MedInc` – Median income in the block group.
2. `HouseAge` – Median house age.
3. `AveRooms` – Average number of rooms.
4. `AveBedrms` – Average number of bedrooms.
5. `Population` – Block group population.
6. `AveOccup` – Average household occupancy.
7. `Latitude` – Geographic latitude.
8. `Longitude` – Geographic longitude.

### Target Variable

- `MedHouseVal` – Median house value in units of $100,000.

**Machine Learning Task:** Regression

**Goal:** Predict the median house value based on housing-related features.

## 🧠 Key Concepts Covered

### 1. XGBoost (Extreme Gradient Boosting)

- XGBoost is an advanced ensemble machine learning algorithm based on gradient boosting.
- It combines multiple decision trees to improve prediction accuracy.
- Each new tree tries to correct the errors made by previous trees.
- It is commonly used for both regression and classification problems.

### 2. Dataset Loading

- Used `fetch_california_housing()` to load the built-in California Housing dataset.
- Converted the dataset into a Pandas DataFrame.
- Separated independent variables (X) and dependent variable (y).

### 3. Train-Test Split

- Used `train_test_split()` to divide the dataset into training and testing sets.
- 80% of the data is used for training.
- 20% of the data is used for testing.
- `random_state=42` ensures reproducibility.

### 4. Feature Scaling

- Used `StandardScaler()` to standardize the input features.
- Transforms features to have a mean of approximately 0 and standard deviation of approximately 1.
- The scaler is fitted on training data and applied to testing data.

### 5. XGBoost Regressor

Used `XGBRegressor()` to build the regression model.

**Important Parameters:**

- `objective='reg:squarederror'` – Uses squared error loss for regression.
- `n_estimators=100` – Builds 100 boosting trees.
- `learning_rate=0.1` – Controls the contribution of each tree.
- `random_state=42` – Ensures reproducibility.

### 6. Model Training

- Used `fit()` to train the XGBoost model.
- The model learns patterns and relationships between housing features and house prices.

### 7. Prediction

- Used `predict()` to generate predictions on the testing dataset.
- Predicted values are compared with actual house prices.

### 8. Model Evaluation

Used the following regression evaluation metrics:

- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Square root of MSE; measures prediction error in the target variable's units.
- **R² Score:** Measures how well the model explains the variation in the target variable. A higher value generally indicates better performance.

### 9. Feature Importance

- Used `feature_importances_` to identify the importance of each input feature.
- Created a bar plot using Seaborn.
- Helps understand which housing features contribute most to predictions.

### 10. Actual vs Predicted Visualization

- Used a scatter plot to compare actual and predicted house prices.
- Added a diagonal reference line representing perfect predictions.
- Points closer to the reference line indicate more accurate predictions.

### 11. Model Saving using Joblib

- Used `joblib.dump()` to save the trained XGBoost model as `xgb_model.pkl`.
- Saved the StandardScaler as `scaler.pkl`.
- These files can be reused later without retraining the model.

### 12. Prediction on New House Data

- Created a custom DataFrame containing new house information.
- Applied the same fitted scaler to the new data.
- Used the trained XGBoost model to predict the house price.

## 🛠️ Tech Stack

- **Python** – Programming language.
- **NumPy** – Numerical operations.
- **Pandas** – Data manipulation and analysis.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical visualization.
- **Scikit-learn** – Dataset loading, train-test splitting, feature scaling, and evaluation metrics.
- **XGBoost** – Gradient boosting regression algorithm.
- **Joblib** – Saving and loading trained models.

## 📈 Machine Learning Operations Performed

| Operation | Function / Class | Purpose |
|---|---|---|
| Dataset Loading | `fetch_california_housing()` | Loads the California Housing dataset |
| DataFrame Creation | `pd.DataFrame()` | Converts dataset features into a DataFrame |
| Train-Test Split | `train_test_split()` | Splits data into training and testing sets |
| Feature Scaling | `StandardScaler()` | Standardizes input features |
| Model Initialization | `XGBRegressor()` | Creates the XGBoost regression model |
| Model Training | `fit()` | Trains the model using training data |
| Prediction | `predict()` | Predicts house prices |
| MSE Calculation | `mean_squared_error()` | Calculates mean squared error |
| RMSE Calculation | `np.sqrt()` | Calculates root mean squared error |
| R² Score | `r2_score()` | Evaluates model performance |
| Feature Importance | `feature_importances_` | Extracts feature importance scores |
| Bar Plot | `sns.barplot()` | Visualizes feature importance |
| Scatter Plot | `plt.scatter()` | Compares actual and predicted values |
| Reference Line | `plt.plot()` | Displays the perfect prediction line |
| Model Saving | `joblib.dump()` | Saves the trained model and scaler |

## 💡 Key Learnings

1. Understood XGBoost and how gradient boosting works.
2. Learned to perform regression using `XGBRegressor`.
3. Practiced loading and preparing a real-world housing dataset.
4. Understood train-test splitting and feature scaling.
5. Learned important XGBoost parameters such as `n_estimators`, `learning_rate`, and `objective`.
6. Evaluated regression models using RMSE and R² Score.
7. Learned to interpret feature importance.
8. Visualized actual and predicted values using scatter plots.
9. Learned to save trained models and scalers using Joblib.
10. Practiced predicting house prices for new custom input data.

## 📁 Project Structure

```
XGBoost-Regression
│
├── XGBoost_Regression.ipynb
│
├── xgb_model.pkl
├── scaler.pkl
│
└── README.md
```

## 🚀 Future Improvements

- Perform hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
- Compare XGBoost with Random Forest, Gradient Boosting, and Linear Regression.
- Evaluate the model using additional regression metrics such as MAE.
- Visualize residuals to understand prediction errors.
- Use cross-validation to evaluate model performance more reliably.
- Build a web application using Streamlit or Flask for interactive house price prediction.
