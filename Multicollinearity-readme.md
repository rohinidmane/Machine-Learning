# 📊 Multicollinearity Detection using Correlation Matrix and VIF

## 📌 Introduction

This project demonstrates how to identify **Multicollinearity** among independent variables using a Correlation Matrix and Variance Inflation Factor (VIF).

Multicollinearity occurs when two or more independent variables in a dataset are highly correlated with each other. It can make regression model coefficients unstable and difficult to interpret.

## 📊 What This Project Does

- Creates a sample dataset using NumPy.
- Generates three independent variables (`X1`, `X2`, and `X3`).
- Creates a highly correlated relationship between `X1` and `X2`.
- Calculates the correlation matrix.
- Calculates the Variance Inflation Factor (VIF) for each feature.
- Identifies multicollinearity among independent variables.

## 🔄 Project Workflow

1. Import the required Python libraries.
2. Set a random seed for reproducibility.
3. Generate three sample variables using NumPy.
4. Create a DataFrame using Pandas.
5. Calculate the correlation matrix.
6. Calculate VIF for each independent variable.
7. Interpret the correlation and VIF values.

## 📁 Dataset Information

**Dataset Type:** Manually created sample dataset

**Number of Records:** 100

**Number of Features:** 3

| Feature | Description                                      |
|---------|--------------------------------------------------|
| `X1`    | Randomly generated numerical variable            |
| `X2`    | Variable generated using `2 * X1 + random noise` |
| `X3`    | Randomly generated independent variable          |

### Relationship Between Variables

- `X1` and `X2` are highly correlated.
- `X3` is generated independently of the other variables.

## 🧠 Key Concepts Covered

### 1. Multicollinearity

Multicollinearity occurs when independent variables are highly correlated with one another.

It can cause:
- Unstable regression coefficients.
- Difficulty interpreting individual feature effects.
- Increased standard errors.
- Reduced reliability of coefficient estimates.

### 2. Correlation Matrix

A correlation matrix shows the strength and direction of relationships between numerical variables.

Correlation values range from -1 to +1.

| Correlation Value | Interpretation               |
|-------------------|------------------------------|
| +1                | Perfect positive correlation |
| 0                 | No linear correlation        |
| -1                | Perfect negative correlation |

In this project, the correlation between `X1` and `X2` is approximately **0.9988**, indicating an extremely strong positive relationship.

### 3. Variance Inflation Factor (VIF)

VIF measures how much the variance of a regression coefficient is increased due to multicollinearity with other independent variables.

**VIF Interpretation:**

| VIF Value       | Interpretation           |
|-----------------|--------------------------|
| 1               | No multicollinearity     |
| Less than 5     | Generally acceptable     |
| 5–10            | High multicollinearity   |
| Greater than 10 | Severe multicollinearity |

### 4. Random Seed

`np.random.seed(10)` ensures that the random values generated are reproducible when the code is executed again.

## 🛠️ Tech Stack

| Technology       | Purpose                              |
|------------------|--------------------------------------|
| Python           | Programming language                 |
| NumPy            | Generating random numerical data     |
| Pandas           | Creating and manipulating DataFrames |
| Statsmodels      | Calculating Variance Inflation Factor|
| Jupyter Notebook | Writing and executing Python code    |

## 📈 Operations Performed

| Function / Method             | Purpose                                   |
|-------------------------------|-------------------------------------------|
| `np.random.seed()`            | Sets the random seed for reproducibility  |
| `np.random.rand()`            | Generates random values between 0 and 1   |
| `pd.DataFrame()`              | Creates a DataFrame                       |
| `df.corr()`                   | Calculates the correlation matrix         |
| `df.columns`                  | Returns the column names                  |
| `df.shape`                    | Returns the number of rows and columns    |
| `variance_inflation_factor()` | Calculates the VIF for a feature          |
| `df.values`                   | Converts the DataFrame into a NumPy array |
| `range()`                     | Generates indices for calculating VIF     |
| `print()`                     | Displays the results                      |

## 📊 Results and Interpretation

The correlation matrix shows that `X1` and `X2` have an extremely strong positive correlation of approximately **0.9988**.

| Variable Relationship | Observation                         |
|-----------------------|-------------------------------------|
| X1 and X2             | Extremely high positive correlation |
| X1 and X3             | No strong correlation expected      |
| X2 and X3             | No strong correlation expected      |

**Key Observations:**

- `X1` and `X2` contain almost the same information.
- `X3` is generated independently.
- High correlation between `X1` and `X2` indicates potential multicollinearity.
- VIF helps measure how strongly each feature is explained by the other features.

*Note: Exact VIF values are not included because they depend on the actual code execution. The commonly used VIF thresholds are general guidelines, not strict rules.*

## 💡 Key Learnings

- Understanding multicollinearity in machine learning and regression.
- Identifying highly correlated independent variables.
- Creating a correlation matrix using Pandas.
- Calculating VIF using Statsmodels.
- Interpreting correlation and VIF values.
- Understanding how multicollinearity affects regression models.

## 📁 Project Structure

```text
Multicollinearity/
│
├── Multicollinearity.ipynb
└── README.md
```

## 🚀 Future Improvements

- Visualize the correlation matrix using a Seaborn heatmap.
- Identify features with high VIF values.
- Remove or combine highly correlated features.
- Recalculate VIF after removing correlated variables.
- Compare regression model performance before and after handling multicollinearity.