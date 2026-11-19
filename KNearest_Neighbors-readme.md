# 🏷️ K-Nearest Neighbors (KNN) – Classification

## 📌 Introduction
K-Nearest Neighbors (KNN) is a supervised machine learning algorithm used for classification and regression tasks.

It classifies a new data point based on the majority class among its K nearest neighbors. KNN is a distance-based algorithm, so feature scaling is important when features have different measurement ranges.

This project explores KNN classification using fruit classification, flower prediction, and the Iris dataset. It also covers Cross-Validation, choosing the optimal K value, Feature Scaling, and model evaluation.

## 📊 What This Project Does
- Creates a sample dataset for fruit classification.
- Classifies a new fruit as Apple or Orange using KNN.
- Experiments with different K values.
- Uses Cross-Validation to compare model accuracy.
- Visualizes accuracy for different K values.
- Loads the Iris dataset from Scikit-learn.
- Splits data into training and testing sets.
- Builds a KNN classification model.
- Predicts flower species using petal measurements.
- Applies Standard Scaling to Iris features.
- Evaluates model performance using accuracy, confusion matrix, and classification report.

## 🔄 KNN Workflow

Load or Create Dataset  
        ↓  
Separate Features and Labels  
        ↓  
Split Data into Training and Testing Sets  
        ↓  
Apply Feature Scaling (where required)  
        ↓  
Initialize KNN Classifier  
        ↓  
Train the Model  
        ↓  
Find K Nearest Neighbors  
        ↓  
Predict Class Using Majority Voting  
        ↓  
Evaluate Model Performance

## 📊 Dataset Information

This project uses three types of datasets.

### 1. Fruit Classification Dataset

A manually created dataset containing fruit characteristics.

**Features:**
- Weight
- Color Score

**Target Classes:**
- Apple
- Orange

**New Fruit:** `[155, 0.72]`

The KNN model uses 3 nearest neighbors to classify the new fruit.

### 2. Iris Dataset

**Dataset:** Iris Dataset

**Source:** Scikit-learn (`load_iris()`)

The dataset contains measurements of three different flower species.

**Features:**
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

**Target Classes:**
- Setosa
- Versicolor
- Virginica

**Data Splitting:**
- Training Data: 70%
- Testing Data: 30%
- Random State: 42

### 3. Custom Flower Classification Dataset

A manually created dataset containing flower measurements.

**Features:**
- Petal Length
- Petal Width

**Target Classes:**
- Setosa
- Versicolor
- Virginica

**New Flower:** `[4.8, 1.6]`

The model uses the 3 nearest known flowers to predict its class.

## 🧠 Key Concepts Covered

### 1. K-Nearest Neighbors (KNN)
- A supervised machine learning algorithm.
- Classifies data based on nearby data points.
- Uses distance calculations to identify nearest neighbors.
- Uses majority voting for classification.

### 2. K Value
- Represents the number of nearest neighbors considered during prediction.
- A small K value can make the model sensitive to noise.
- A large K value can make the model less sensitive to local patterns.
- Choosing an appropriate K value helps improve model performance.

### 3. Euclidean Distance
Euclidean Distance measures the straight-line distance between two data points.

Formula:

\[
d(x,y)=\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}
\]

### 4. Cross-Validation
- Evaluates model performance using multiple data splits.
- Divides the dataset into different folds.
- Helps compare different K values.
- Provides a more reliable estimate of model performance.

### 5. Standard Scaling
- Standardizes features using mean and standard deviation.
- Produces features with approximately zero mean and unit variance.
- Important for distance-based algorithms like KNN.
- Helps prevent features with larger numerical values from dominating distance calculations.

### 6. Model Evaluation

- **Accuracy:** Measures the percentage of correct predictions.
- **Confusion Matrix:** Displays correct and incorrect predictions for each class.
- **Precision:** Measures how many predicted positive cases are actually positive.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1-Score:** Represents the balance between precision and recall.
- **Macro Average:** Calculates the average of class-wise metrics equally.
- **Weighted Average:** Calculates the average of class-wise metrics based on the number of samples in each class.

## 🛠️ Tech Stack

- Python
- NumPy
- Matplotlib
- Scikit-learn

## 📈 Operations Performed

| Operation                 | Description                                            |
|---------------------------|--------------------------------------------------------|
| `np.array()`              | Creates feature and label arrays.                      |
| `KNeighborsClassifier()`  | Initializes the KNN classification model.              |
| `fit()`                   | Trains the KNN model.                                  |
| `predict()`               | Predicts the class of new data points.                 |
| `cross_val_score()`       | Evaluates model performance using Cross-Validation.    |
| `range()`                 | Generates different K values for experimentation.      |
| `plt.plot()`              | Visualizes accuracy for different K values.            |
| `load_iris()`             | Loads the Iris dataset.                                |
| `train_test_split()`      | Splits data into training and testing sets.            |
| `StandardScaler()`        | Standardizes numerical features.                       |
| `fit_transform()`         | Learns scaling parameters and transforms training data.|
| `transform()`             | Applies the learned scaling to testing data.           |
| `accuracy_score()`        | Calculates model accuracy.                             |
| `confusion_matrix()`      | Generates the confusion matrix.                        |
| `classification_report()` | Displays precision, recall, F1-score, and support.     |

## 💡 Key Learnings

1. Understood the working of the K-Nearest Neighbors algorithm.
2. Learned how KNN classifies new data points using nearest neighbors.
3. Practiced fruit classification using weight and color score.
4. Learned how to predict flower species using petal measurements.
5. Understood the importance of choosing an appropriate K value.
6. Practiced Cross-Validation to compare different K values.
7. Learned why Feature Scaling is important for distance-based algorithms.
8. Applied Standard Scaling to the Iris dataset.
9. Evaluated classification performance using accuracy, confusion matrix, precision, recall, and F1-score.
10. Understood Macro Average and Weighted Average in classification reports.

## 📁 Project Structure

```
KNN-Classification
│
├── KNN_Classification.ipynb
└── README.md
```

## 🚀 Future Improvements

- Experiment with different K values.
- Compare different distance metrics.
- Explore different KNN weighting methods.
- Compare model performance with and without feature scaling.
- Apply KNN to other real-world datasets.
- Use GridSearchCV to find the best K value and model parameters.
- Compare KNN with Decision Tree, Logistic Regression, and other classification algorithms.