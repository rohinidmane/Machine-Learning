# 💧 Water Quality Prediction using Random Forest Classifier

This project demonstrates the implementation of a Random Forest Classification algorithm to predict whether water is safe or unsafe for drinking based on different water quality parameters. It uses the Water Quality dataset and includes data cleaning, exploratory data analysis, handling invalid values, class imbalance analysis, resampling, model training, and prediction.

## 📊 What This Project Does

- Downloads the Water Quality dataset using KaggleHub.
- Loads the dataset using Pandas.
- Explores dataset information and statistical summaries.
- Checks for duplicate records.
- Identifies and removes invalid values (`#NUM!`) from the ammonia column.
- Converts ammonia and target columns into numerical data types.
- Performs Exploratory Data Analysis (EDA).
- Visualizes water quality parameter distributions for safe and unsafe water.
- Analyzes the distribution of safe and unsafe water categories.
- Identifies class imbalance in the dataset.
- Separates input features and target variable.
- Applies resampling to balance the dataset.
- Builds a Random Forest Classifier.
- Trains the model and predicts water safety.
- Predicts whether new water samples are safe or unsafe.

## 🔄 Machine Learning Workflow

Import Required Libraries  
        ⬇
Download Water Quality Dataset  
        ⬇  
Load Dataset  
        ⬇  
Data Exploration  
        ⬇  
Data Cleaning and Preprocessing  
        ⬇  
Handle Invalid Values  
        ⬇  
Exploratory Data Analysis (EDA)  
        ⬇  
Analyze Class Distribution  
        ⬇  
Identify Class Imbalance  
        ⬇  
Separate Input Features and Target Variable  
        ⬇  
Apply Resampling  
        ⬇  
Train-Test Split  
        ⬇  
Initialize Random Forest Classifier  
        ⬇  
Train the Model  
        ⬇  
Make Predictions  
        ⬇ 
Model Evaluation  
        ⬇  
Predict Water Safety for New Samples

## 📊 Dataset Information

- **Dataset Name:** Water Quality Dataset
- **Source:** Kaggle
- **Dataset Identifier:** `mssmartypants/water-quality`
- **File Name:** `waterQuality1.csv`
- **Target Variable:** `is_safe`
- **Problem Type:** Binary Classification

**Input Features:**

The dataset contains water quality parameters, including:

- Aluminium
- Ammonia
- Arsenic
- Barium
- Cadmium
- Chloramine
- Chromium
- Copper
- Flouride
- Bacteria
- Viruses
- Lead
- Nitrates
- Nitrites
- Mercury
- Perchlorate
- Radium
- Selenium
- Silver
- Uranium

**Target Variable:**

- `is_safe = 1` – Safe Water
- `is_safe = 0` – Unsafe Water

## 🧠 Key Concepts Covered

### 1. Data Loading using KaggleHub

- Understanding how to download datasets directly from Kaggle.
- Using `kagglehub.dataset_download()` to download the Water Quality dataset.
- Loading CSV files using `pd.read_csv()`.

### 2. Data Exploration

- Understanding dataset structure using `df.info()`.
- Generating statistical summaries using `df.describe()`.
- Checking column names using `df.columns`.
- Identifying duplicate records using `df.duplicated().sum()`.

### 3. Data Cleaning and Preprocessing

- Identifying invalid values in the ammonia column.
- Detecting `#NUM!` values.
- Removing rows containing invalid ammonia values.
- Converting columns into numerical data types using `pd.to_numeric()`.
- Checking the updated dataset information.

### 4. Exploratory Data Analysis (EDA)

- Understanding water quality parameter distributions.
- Creating histograms using Matplotlib.
- Comparing parameter distributions for safe and unsafe water.
- Using different colors to distinguish safe and unsafe categories.
- Understanding the frequency distribution of water quality features.

### 5. Class Distribution Analysis

- Counting safe and unsafe water records.
- Visualizing target class distribution using a pie chart.
- Identifying class imbalance in the dataset.
- Understanding how imbalanced data can affect classification models.

### 6. Feature Selection

- Separating independent variables and dependent variables.
- Using `df.iloc[:,:-1]` to select input features.
- Using `df.iloc[:,-1]` to select the target variable.
- Preparing the dataset for machine learning.

### 7. Resampling Techniques

- Understanding the importance of balancing an imbalanced dataset.
- Applying a resampling technique to balance safe and unsafe water categories.
- Comparing original and resampled dataset sizes.
- Understanding how balanced data can help improve classification performance.

### 8. Random Forest Classification

- Understanding the Random Forest ensemble learning algorithm.
- Learning how multiple Decision Trees work together.
- Initializing the classifier using `RandomForestClassifier()`.
- Training the model using `fit()`.
- Predicting water safety using `predict()`.

### 9. Model Evaluation

- Generating predictions using test data.
- Evaluating classification performance using `classification_report()`.
- Understanding precision, recall, F1-score, and support.
- Analyzing the model's ability to identify safe and unsafe water.

### 10. New Water Sample Prediction

- Providing new water quality parameter values as input.
- Passing sample data in a 2-dimensional array format.
- Predicting whether the given water sample is safe or unsafe.
- Understanding how a trained Random Forest model can classify new observations.

## 🛠️ Tech Stack

- **Python** – Programming language
- **NumPy** – Numerical operations
- **Pandas** – Data loading, cleaning, and manipulation
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Scikit-learn** – Machine learning implementation
- **KaggleHub** – Dataset downloading
- **Random Forest Classifier** – Classification algorithm
- **Jupyter Notebook** – Writing and executing Python code

## 📈 Machine Learning Operations Performed

| Operation               | Function / Class         | Purpose                                          |
|-------------------------|--------------------------|--------------------------------------------------|
| Dataset Download        | `kagglehub.dataset_download()`| Downloads the dataset from Kaggle           |
| Dataset Loading         | `pd.read_csv()`           | Loads the CSV file                              |
| Dataset Information     | `df.info()`               | Displays dataset structure and data types       |
| Statistical Summary     | `df.describe()`           | Generates descriptive statistics                |
| Duplicate Checking      | `df.duplicated().sum()`   | Counts duplicate records                        |
| Invalid Value Filtering |`df[df['ammonia']=='#NUM!]`| Identifies invalid ammonia values               |
| Data Type Conversion    | `pd.to_numeric()`         | Converts columns into numerical format          |
| Histogram               | `plt.hist()`              | Visualizes feature distributions                |
| Pie Chart               | `plt.pie()`               | Displays safe and unsafe class distribution     |
| Feature Selection       | `df.iloc[:,:-1]`          | Selects independent variables                   |
| Target Selection        | `df.iloc[:,-1]`           | Selects the dependent variable                  |
| Resampling              | `fit_resample()`          | Resamples the dataset to address class imbalance|
| Model Initialization    | `RandomForestClassifier()`| Creates the Random Forest model                 |
| Model Training          | `fit()`                   | Trains the classifier                           |
| Prediction              | `predict()`               | Predicts safe or unsafe water                   |
| Model Evaluation        | `classification_report()` | Evaluates classification performance            |

## 💡 Key Learnings

1. Learned how to download datasets using KaggleHub.
2. Practiced loading and exploring real-world datasets using Pandas.
3. Understood how to identify and handle invalid numerical values.
4. Learned data cleaning and numerical data type conversion.
5. Practiced Exploratory Data Analysis using Matplotlib.
6. Learned how to compare feature distributions between two classes.
7. Understood class imbalance and its impact on machine learning models.
8. Learned the importance of resampling techniques.
9. Understood the working of the Random Forest classification algorithm.
10. Practiced training and testing a classification model.
11. Learned how to evaluate classification performance using a classification report.
12. Practiced predicting water safety using new input samples.

## 📁 Project Structure

```
Water_Quality_Prediction/
│
├── waterQuality1.csv
├── Water_Quality_Prediction.ipynb
└── README.md
```

## 🚀 Future Improvements

- Apply KNN Imputation to handle missing values.
- Compare different resampling techniques such as SMOTE and Random Oversampling.
- Use a stratified train-test split.
- Apply feature scaling where required by the selected algorithms.
- Tune Random Forest hyperparameters.
- Evaluate the model using a confusion matrix, accuracy, precision, recall, and F1-score.
- Compare Random Forest with Decision Tree, Logistic Regression, and XGBoost.
- Visualize feature importance to identify the most influential water quality parameters.
- Test the model on additional water quality samples.