# 🌸 Iris Flower Classification using Gaussian Naive Bayes

This project demonstrates the implementation of the Gaussian Naive Bayes classification algorithm using Python and Scikit-learn. It uses the Iris dataset to classify flower species based on sepal and petal measurements. The project also includes model training, evaluation, and prediction of new flower samples.

## 📊 What This Project Does

- Loads the Iris dataset from `Iris.csv` using Pandas.
- Selects four flower measurement features as input variables.
- Selects `Species` as the target variable.
- Splits the dataset into training and testing sets.
- Initializes a Gaussian Naive Bayes classifier.
- Trains the model using the training dataset.
- Predicts flower species for test data.
- Evaluates model performance using a classification report and confusion matrix.
- Predicts the species of a new flower sample.

## 🔄 Machine Learning Workflow

Load Iris Dataset  
        ⬇
Data Preparation  
        ⬇ 
Select Input Features and Target Variable  
        ⬇  
Train-Test Split  
        ⬇  
Initialize Gaussian Naive Bayes Classifier  
        ⬇  
Train the Model  
        ⬇  
Make Predictions  
        ⬇  
Model Evaluation  
        ⬇  
Predict New Flower Samples

## 📊 Dataset Information

- **Dataset Name:** Iris Dataset
- **File Name:** `Iris.csv`
- **Source:** External CSV file
- **Total Samples:** 150 (standard Iris dataset)
- **Features:** 4
- **Target Variable:** Species
- **Target Classes:** 3

**Input Features:**

- Sepal Length (`SepalLengthCm`)
- Sepal Width (`SepalWidthCm`)
- Petal Length (`PetalLengthCm`)
- Petal Width (`PetalWidthCm`)

**Target Classes:**

- Iris-setosa
- Iris-versicolor
- Iris-virginica

## 🧠 Key Concepts Covered

### 1. Gaussian Naive Bayes Algorithm

- Understanding the Naive Bayes classification algorithm.
- Learning how Bayes' Theorem is used for classification.
- Understanding the assumption of independence between input features.
- Learning how Gaussian Naive Bayes handles continuous numerical data.
- Understanding how the algorithm uses a Gaussian (normal) distribution to calculate probabilities.

### 2. Iris Dataset

- Loading the Iris dataset using `pd.read_csv()`.
- Understanding the four flower measurement features.
- Separating input features and target labels.
- Working with multiclass classification.

### 3. Independent and Dependent Variables

- Selecting four measurement columns as input features (`X`).
- Selecting `Species` as the target variable (`y`).
- Understanding the role of features in predicting flower species.

### 4. Train-Test Split

- Splitting the dataset using `train_test_split()`.
- Using 70% of the data for training and 30% for testing.
- Setting `random_state=42` for reproducibility.

### 5. Gaussian Naive Bayes Model

- Initializing the classifier using `GaussianNB()`.
- Understanding Gaussian probability distribution.
- Applying Naive Bayes to continuous numerical features.

### 6. Model Training

- Training the Gaussian Naive Bayes model using `fit()`.
- Learning how the model estimates probabilities from training data.
- Preparing the trained model for classification.

### 7. Model Prediction

- Predicting flower species using `predict()`.
- Making predictions on unseen test data.
- Providing new flower measurements as input.
- Predicting the species for the sample `[3, 4, 2, 0.5]`.

### 8. Model Evaluation

- Evaluating model performance using `classification_report()`.
- Understanding precision, recall, and F1-score.
- Generating a confusion matrix using `confusion_matrix()`.
- Analyzing correct and incorrect predictions.

## 🛠️ Tech Stack

- **Python** – Programming language
- **Pandas** – Data loading and manipulation
- **Scikit-learn** – Machine learning implementation and evaluation
- **Gaussian Naive Bayes** – Classification algorithm
- **Jupyter Notebook** – Writing and executing Python code

## 📈 Machine Learning Operations Performed

| Operation                | Function / Class          | Purpose                                        |
|--------------------------|---------------------------|------------------------------------------------|
| Dataset Loading          | `pd.read_csv()`           | Loads the Iris dataset                         |
| Column Selection         | `df.columns`              | Displays dataset column names                  |
| Feature Selection        | `df[[...]]`               | Selects input features                         |
| Target Selection         | `df['Species']`           | Selects the target variable                    |
| Data Splitting           | `train_test_split()`      | Splits data into training and testing sets     |
| Model Initialization     | `GaussianNB()`            | Creates the Gaussian Naive Bayes classifier    |
| Model Training           | `fit()`                   | Trains the classifier                          |
| Prediction               | `predict()`               | Predicts flower species                        |
| Classification Report    | `classification_report()` | Evaluates precision, recall, and F1-score      |
| Confusion Matrix         | `confusion_matrix()`      | Displays correct and incorrect classifications |
| Data Preview             | `df.head()`               | Displays the first five rows of the dataset    |

## 💡 Key Learnings

1. Learned the fundamentals of the Naive Bayes classification algorithm.
2. Understood Bayes' Theorem and the independence assumption.
3. Learned how Gaussian Naive Bayes handles continuous numerical features.
4. Practiced loading and preparing a dataset using Pandas.
5. Learned how to separate input features and target variables.
6. Understood how to split data into training and testing sets.
7. Practiced training a Gaussian Naive Bayes classifier.
8. Learned how to predict flower species using new input values.
9. Evaluated model performance using classification reports and confusion matrices.
10. Understood how Naive Bayes can be applied to multiclass classification problems.

## 📁 Project Structure

```text
Gaussian_Naive_Bayes_Iris/
│
├── Iris.csv
├── Gaussian_Naive_Bayes.ipynb
└── README.md
```

## 🚀 Future Improvements

- Perform Exploratory Data Analysis (EDA).
- Visualize relationships between flower measurement features.
- Compare Gaussian Naive Bayes with other classification algorithms.
- Evaluate model performance using accuracy, precision, recall, and F1-score.
- Experiment with different train-test split ratios.
- Apply Gaussian Naive Bayes to other classification datasets.