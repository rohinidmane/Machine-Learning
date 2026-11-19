# 🌸 AdaBoost Classification using Iris Dataset

This project demonstrates the AdaBoost (Adaptive Boosting) ensemble machine learning algorithm using Python and Scikit-learn. It uses the Iris dataset to perform both binary and multiclass classification with Decision Tree as the base estimator. The project also includes model evaluation and prediction of new flower samples.

## 📊 What This Project Does

- Loads the Iris dataset using Scikit-learn.
- Performs binary classification using two Iris classes.
- Performs multiclass classification using all three Iris classes.
- Splits the dataset into training and testing sets.
- Uses Decision Tree as the base estimator.
- Builds an AdaBoost classifier with 50 estimators.
- Trains the AdaBoost model.
- Evaluates model performance using accuracy and classification report.
- Predicts flower species for new input values.

## 🔄 Machine Learning Workflow

Load Iris Dataset  
        ⬇  
Data Preparation  
        ⬇  
Binary and Multiclass Classification  
        ⬇  
Train-Test Split  
        ⬇  
Initialize Decision Tree Base Estimator  
        ⬇  
Initialize AdaBoost Classifier  
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
- **Source:** Scikit-learn built-in dataset
- **Total Samples:** 150
- **Features:** 4
- **Target Classes:** 3

**Features:**
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

**Target Classes:**
- Setosa
- Versicolor
- Virginica

**Classification Tasks:**

| Task                      | Classes Used                      |
|---------------------------|-----------------------------------|
| Binary Classification     | Setosa and Versicolor             |
| Multiclass Classification | Setosa, Versicolor, and Virginica |

## 🧠 Key Concepts Covered

### 1. AdaBoost Algorithm
- Understanding Adaptive Boosting.
- Learning how AdaBoost combines multiple weak learners to create a strong classifier.
- Understanding how the algorithm gives more attention to incorrectly classified samples.
- Using multiple estimators to improve classification performance.

### 2. Iris Dataset
- Loading the Iris dataset using `load_iris()`.
- Separating input features and target labels.
- Understanding the four flower measurement features.
- Working with binary and multiclass classification.

### 3. Binary Classification
- Selecting only Setosa and Versicolor classes.
- Removing the third class using conditional filtering.
- Building an AdaBoost model for two-class classification.

### 4. Multiclass Classification
- Using all three Iris flower classes.
- Training AdaBoost to predict Setosa, Versicolor, and Virginica.
- Understanding multiclass classification.

### 5. Train-Test Split
- Splitting the dataset using `train_test_split()`.
- Using 70% data for training and 30% for testing.
- Setting `random_state=42` for reproducibility.

### 6. Decision Tree as Base Estimator
- Using `DecisionTreeClassifier()` as the base learner.
- Setting `max_depth=1` to create a decision stump.
- Understanding how AdaBoost combines weak learners.

### 7. Model Training
- Initializing `AdaBoostClassifier()`.
- Using `n_estimators=50`.
- Setting `learning_rate=1.0`.
- Training the model using `fit()`.

### 8. Model Evaluation
- Predicting test data using `predict()`.
- Calculating accuracy using `accuracy_score()`.
- Evaluating precision, recall, and F1-score using `classification_report()`.

### 9. New Flower Prediction
- Providing new flower measurements as input.
- Predicting the flower class using the trained model.
- Converting predicted numerical labels into flower names using `iris.target_names`.

## 🛠️ Tech Stack

- **Python** – Programming language
- **NumPy** – Numerical operations
- **Pandas** – Data manipulation
- **Scikit-learn** – Machine learning and model evaluation

## 📈 Machine Learning Operations Performed

| Operation             | Function / Class           | Purpose                                    |
|-----------------------|----------------------------|--------------------------------------------|
| Dataset Loading       | `load_iris()`              | Loads the Iris dataset                     |
| Data Splitting        | `train_test_split()`       | Splits data into training and testing sets |
| Base Estimator        | `DecisionTreeClassifier()` | Creates a weak learner                     |
| AdaBoost Model        | `AdaBoostClassifier()`     | Builds the boosting classifier             |
| Model Training        | `fit()`                    | Trains the classifier                      |
| Prediction            | `predict()`                | Predicts flower classes                    |
| Accuracy              | `accuracy_score()`         | Measures classification accuracy           |
| Classification Report | `classification_report()`  | Evaluates precision, recall, and F1-score  |

## 💡 Key Learnings

1. Learned the fundamentals of the AdaBoost algorithm.
2. Understood the concept of ensemble learning.
3. Learned how weak learners are combined to build a strong classifier.
4. Practiced binary and multiclass classification.
5. Understood the role of Decision Tree as a base estimator.
6. Learned how to split data into training and testing sets.
7. Evaluated model performance using accuracy and classification reports.
8. Practiced predicting new flower species using a trained model.
9. Understood how AdaBoost can be applied to classification problems.

## 📁 Project Structure

```text
AdaBoost_Iris_Classification/
│
├── AdaBoost.ipynb
└── README.md
```

## 🚀 Future Improvements

- Compare AdaBoost with Random Forest and Gradient Boosting.
- Experiment with different values of `n_estimators`.
- Tune the learning rate to improve model performance.
- Visualize decision boundaries.
- Apply AdaBoost to other real-world classification datasets.