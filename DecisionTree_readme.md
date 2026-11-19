# 🌳 Decision Tree Classification – Iris Dataset

## 📌 Introduction
A Decision Tree is a supervised machine learning algorithm used for classification and regression tasks. It makes decisions by splitting data into branches based on feature values.

This project uses the Iris dataset to build a Decision Tree Classification model and evaluate its performance using different evaluation metrics. It also explores mathematical calculations related to Entropy and Information Gain.

## 📊 What This Project Does
- Loads the Iris dataset from Scikit-learn.
- Splits the dataset into training and testing sets.
- Builds a Decision Tree Classifier.
- Trains the model using the Gini impurity criterion.
- Predicts flower species using test data.
- Evaluates model performance using accuracy, confusion matrix, and classification report.
- Visualizes the confusion matrix and decision tree.
- Performs manual calculations of Entropy and Information Gain.

## 🔄 Decision Tree Workflow

Load Iris Dataset  
        ↓  
Separate Features and Target  
        ↓  
Split Data into Training and Testing Sets  
        ↓  
Initialize Decision Tree Classifier  
        ↓  
Train the Model  
        ↓  
Make Predictions  
        ↓  
Evaluate Model Performance  
        ↓  
Visualize Confusion Matrix and Decision Tree

## 📊 Dataset Information

**Dataset:** Iris Dataset

The Iris dataset contains measurements of three different flower species.

- Setosa
- Versicolor
- Virginica

**Features:**
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

**Target:** Iris flower species

**Data Splitting:**
- Training Data: 70%
- Testing Data: 30%
- Random State: 42

## 🧠 Key Concepts Covered

- **Decision Tree:** A supervised learning algorithm that makes predictions using a tree-like structure.
- **Gini Impurity:** Measures the impurity of a dataset and helps determine the best split.
- **Entropy:** Measures the uncertainty or impurity in a dataset.
- **Information Gain:** Measures the reduction in entropy after splitting the dataset.
- **Root Node:** The first and main decision node of a tree.
- **Decision Node:** A node where data is divided based on a condition.
- **Leaf Node:** The final node that represents the predicted class.
- **Overfitting:** When a model learns the training data too closely and performs poorly on unseen data.

## 🛠️ Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Math

## 📈 Operations Performed

| Operation                  | Description                                                |
|----------------------------|------------------------------------------------------------|
| `load_iris()`              | Loads the Iris dataset.                                    |
| `train_test_split()`       | Splits data into training and testing sets.                |
| `DecisionTreeClassifier()` | Creates the Decision Tree classification model.            |
| `fit()`                    | Trains the model using training data.                      |
| `predict()`                | Predicts flower classes for test data.                     |
| `accuracy_score()`         | Calculates model accuracy.                                 |
| `confusion_matrix()`       | Creates a confusion matrix.                                |
| `ConfusionMatrixDisplay()` | Displays the confusion matrix visually.                    |
| `classification_report()`  | Displays precision, recall, F1-score, and support.         |
| `plot_tree()`              | Visualizes the trained Decision Tree.                      |
| `math.log2()`              | Calculates logarithm with base 2 for entropy calculations. |

## 🧮 Entropy and Information Gain Calculations

This project also includes manual mathematical calculations related to Decision Tree splitting.

**1. Entropy**

Entropy measures the uncertainty or impurity in a dataset.

Formula:

Entropy = - Σ (p × log₂(p))

Where:
- `p` represents the probability of each class.
- `log₂` represents logarithm with base 2.

**2. Information Gain**

Information Gain measures how much entropy decreases after splitting a dataset.

Formula:

Information Gain = Parent Entropy - Weighted Child Entropy

These calculations help understand how a Decision Tree selects the best feature for splitting data.

## 💡 Key Learnings

1. Understood the working of Decision Tree Classification.
2. Learned how to load and work with the Iris dataset.
3. Practiced splitting data into training and testing sets.
4. Understood Gini impurity and its role in decision-making.
5. Learned the concepts of Entropy and Information Gain.
6. Evaluated classification models using accuracy, confusion matrix, precision, recall, and F1-score.
7. Learned to visualize a confusion matrix and Decision Tree.
8. Understood how `max_depth` controls the complexity of a Decision Tree.

## 📁 Project Structure

```
Decision-Tree-Classification/
│
├── Decision_Tree.ipynb
└── README.md
```

## 🚀 Future Improvements

- Experiment with different `max_depth` values.
- Compare Gini impurity and Entropy criteria.
- Apply Decision Tree Classification to other datasets.
- Tune model parameters to improve performance.
- Compare Decision Tree with Random Forest and other classification algorithms.
