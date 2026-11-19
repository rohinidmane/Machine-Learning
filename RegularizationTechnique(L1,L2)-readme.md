# 📊 L1 and L2 Regularization using Ridge and Lasso Regression

This project demonstrates two important regularization techniques in machine learning: **L1 Regularization (Lasso Regression)** and **L2 Regularization (Ridge Regression)** using Python and Scikit-learn. It uses the California Housing dataset to understand how regularization helps reduce overfitting, control model coefficients, and improve model generalization. The project also compares Ridge and Lasso regression using Mean Squared Error (MSE).

## 📊 What This Project Does

- Loads the California Housing dataset using Scikit-learn.
- Separates input features and target variable.
- Splits the dataset into training and testing sets.
- Implements Ridge Regression using L2 regularization.
- Implements Lasso Regression using L1 regularization.
- Applies StandardScaler using a Scikit-learn Pipeline for Lasso.
- Trains both regularized regression models.
- Predicts housing prices using test data.
- Evaluates model performance using Mean Squared Error.
- Extracts and analyzes regression coefficients.
- Understands how Ridge shrinks coefficients and how Lasso can make some coefficients exactly zero.

## 🔄 Machine Learning Workflow

Load California Housing Dataset  
⬇️  
Data Preparation  
⬇️  
Separate Input Features and Target Variable  
⬇️  
Train-Test Split  
⬇️  
Initialize Ridge Regression Model  
⬇️  
Train Ridge Model using L2 Regularization  
⬇️  
Make Ridge Predictions  
⬇️  
Calculate Ridge Mean Squared Error  
⬇️  
Extract Ridge Coefficients  
⬇️  
Initialize StandardScaler and Lasso Pipeline  
⬇️  
Train Lasso Model using L1 Regularization  
⬇️  
Make Lasso Predictions  
⬇️  
Calculate Lasso Mean Squared Error  
⬇️  
Extract Lasso Coefficients  
⬇️  
Compare Regularization Techniques

## 📊 Dataset Information

- **Dataset Name:** California Housing Dataset
- **Source:** Scikit-learn built-in dataset
- **Total Samples:** 20,640
- **Features:** 8
- **Target Variable:** Median House Value
- **Problem Type:** Regression

**Input Features:**

- `MedInc` – Median income in the block group.
- `HouseAge` – Median house age.
- `AveRooms` – Average number of rooms per household.
- `AveBedrms` – Average number of bedrooms per household.
- `Population` – Block group population.
- `AveOccup` – Average number of household members.
- `Latitude` – Geographical latitude.
- `Longitude` – Geographical longitude.

**Target Variable:**

- `MedHouseVal` – Median house value expressed in units of $100,000.

## 🧠 Key Concepts Covered

### 1. Regularization

- Understanding regularization in machine learning.
- Learning how regularization helps reduce overfitting.
- Understanding how penalty terms control model coefficients.
- Learning how regularization improves model generalization.
- Comparing L1 and L2 regularization techniques.

### 2. Ridge Regression (L2 Regularization)

- Understanding L2 regularization.
- Using `Ridge()` to build a Ridge Regression model.
- Applying a penalty based on the squared values of coefficients.
- Understanding how Ridge shrinks coefficient values.
- Learning that Ridge generally does not make coefficients exactly zero.
- Using `alpha=1.0` to control regularization strength.

**Alpha Parameter:**

- `alpha = 0` – No regularization; behaves like ordinary linear regression.
- Higher alpha values – Stronger regularization.
- Very high alpha values – Can lead to underfitting.

### 3. Lasso Regression (L1 Regularization)

- Understanding L1 regularization.
- Using `Lasso()` to build a Lasso Regression model.
- Applying a penalty based on the absolute values of coefficients.
- Understanding how Lasso can shrink some coefficients exactly to zero.
- Learning how Lasso performs automatic feature selection.
- Using `alpha=0.001` for regularization.

**Practical Uses of L1 Regularization:**

- Selecting important predictors in medical and biological datasets.
- Working with text data containing thousands of features.
- Building simpler and more interpretable models.
- Handling high-dimensional datasets.

### 4. Train-Test Split

- Splitting the dataset using `train_test_split()`.
- Using 80% data for training and 20% for testing.
- Setting `random_state=42` for reproducibility.
- Evaluating models on unseen test data.

### 5. Feature Scaling

- Understanding the importance of feature scaling.
- Applying `StandardScaler()` to standardize input features.
- Transforming features to have approximately zero mean and unit variance.
- Understanding why scaling is important for regularized regression models.

### 6. Pipeline

- Understanding Scikit-learn Pipeline.
- Combining feature scaling and Lasso Regression into one workflow.
- Using `Pipeline()` to apply preprocessing and model training sequentially.
- Accessing the trained Lasso model using `named_steps`.

### 7. Model Training and Prediction

- Training Ridge Regression using `fit()`.
- Training Lasso Regression through the pipeline.
- Predicting housing values using `predict()`.
- Understanding how trained regression models make numerical predictions.

### 8. Model Evaluation

- Evaluating regression performance using Mean Squared Error (MSE).
- Understanding that lower MSE indicates smaller average squared prediction errors.
- Comparing Ridge and Lasso model performance.
- Understanding how regularization affects prediction performance.

### 9. Coefficient Analysis

- Extracting Ridge coefficients using `ridge.coef_`.
- Extracting Lasso coefficients using `named_steps['lasso'].coef_`.
- Understanding how Ridge reduces coefficient magnitudes.
- Understanding how Lasso can eliminate less important features by assigning zero coefficients.

## 🛠️ Tech Stack

- **Python** – Programming language
- **NumPy** – Numerical operations
- **Pandas** – Data manipulation and analysis
- **Scikit-learn** – Machine learning implementation
- **Ridge Regression** – L2 regularization
- **Lasso Regression** – L1 regularization
- **StandardScaler** – Feature scaling
- **Pipeline** – Combining preprocessing and model training
- **Mean Squared Error** – Regression model evaluation
- **Jupyter Notebook** – Writing and executing Python code

## 📈 Machine Learning Operations Performed

| Operation | Function / Class | Purpose |
|---|---|---|
| Dataset Loading | `fetch_california_housing()` | Loads the California Housing dataset |
| DataFrame Creation | `pd.DataFrame()` | Creates a DataFrame using dataset features |
| Feature and Target Selection | `data.data`, `data.target` | Separates input features and target values |
| Data Splitting | `train_test_split()` | Splits data into training and testing sets |
| Ridge Model Initialization | `Ridge()` | Creates the L2 regularized regression model |
| Ridge Model Training | `fit()` | Trains the Ridge Regression model |
| Ridge Prediction | `predict()` | Predicts housing values using Ridge Regression |
| Lasso Model Initialization | `Lasso()` | Creates the L1 regularized regression model |
| Feature Scaling | `StandardScaler()` | Standardizes input features |
| Pipeline Creation | `Pipeline()` | Combines scaling and Lasso Regression |
| Lasso Model Training | `fit()` | Trains the Lasso Regression model |
| Lasso Prediction | `predict()` | Predicts housing values using Lasso Regression |
| Model Evaluation | `mean_squared_error()` | Calculates Mean Squared Error |
| Ridge Coefficients | `ridge.coef_` | Extracts Ridge regression coefficients |
| Lasso Coefficients | `lasso_pipeline.named_steps['lasso'].coef_` | Extracts Lasso regression coefficients |

## 💡 Key Learnings

1. Learned the fundamentals of regularization in machine learning.
2. Understood the difference between L1 and L2 regularization.
3. Learned how Ridge Regression reduces coefficient magnitudes.
4. Understood how Lasso Regression performs automatic feature selection.
5. Practiced building regression models using Scikit-learn.
6. Learned the importance of feature scaling in regularized models.
7. Understood how to combine preprocessing and model training using Pipeline.
8. Practiced evaluating regression models using Mean Squared Error.
9. Learned how to extract and interpret model coefficients.
10. Understood how regularization helps control overfitting and improve model generalization.

## 📁 Project Structure

```
L1_L2_Regularization
│
├── Ridge_Lasso_Regression.ipynb
└── README.md
```

## 🚀 Future Improvements

- Compare Linear Regression, Ridge Regression, and Lasso Regression.
- Experiment with different alpha values.
- Visualize coefficient changes for different regularization strengths.
- Apply Elastic Net Regression, which combines L1 and L2 penalties.
- Use cross-validation to select the optimal alpha value.
- Compare model performance using MSE, RMSE, and R-squared.
- Identify important features using Lasso coefficients.