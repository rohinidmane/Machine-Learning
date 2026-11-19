# 🌸 Support Vector Machine (SVM) Classification using Iris Dataset

This project demonstrates the implementation of the Support Vector Machine (SVM) algorithm using Python and Scikit-learn. It uses the Iris dataset to perform binary and multiclass classification. The project includes model training, feature scaling, accuracy evaluation with different random states, and visualization of decision boundaries using different flower features.

## 📊 What This Project Does

- Loads the Iris dataset using Pandas and Scikit-learn.
- Selects four flower measurement features for classification.
- Performs binary and multiclass classification.
- Splits the dataset into training and testing sets.
- Builds an SVM classifier using `SVC()`.
- Trains the SVM model using different datasets and feature combinations.
- Applies StandardScaler for feature scaling.
- Uses a linear kernel for decision boundary visualization.
- Evaluates model performance using accuracy score and classification report.
- Generates a confusion matrix for classification evaluation.
- Tests model accuracy using different random states from 1 to 100.
- Visualizes SVM decision boundaries using two selected features.

## 🔄 Machine Learning Workflow

Load Iris Dataset  
      ⬇️  
Data Preparation  
      ⬇️  
Select Input Features and Target Variable  
      ⬇️  
Binary and Multiclass Classification  
      ⬇️  
Train-Test Split  
      ⬇️  
Initialize SVM Classifier  
      ⬇️  
Feature Scaling  
      ⬇️  
Train the SVM Model  
      ⬇️  
Make Predictions  
      ⬇️  
Model Evaluation  
      ⬇️  
Test Different Random States  
      ⬇️  
Visualize Decision Boundaries

## 📊 Dataset Information

- **Dataset Name:** Iris Dataset
- **Source:** Scikit-learn built-in dataset and external CSV file (`Iris.csv`)
- **Total Samples:** 150
- **Features:** 4
- **Target Classes:** 3
- **Problem Type:** Binary and Multiclass Classification

**Input Features:**

- Sepal Length (`SepalLengthCm`)
- Sepal Width (`SepalWidthCm`)
- Petal Length (`PetalLengthCm`)
- Petal Width (`PetalWidthCm`)

**Target Classes:**

- Setosa
- Versicolor
- Virginica

**Classification Tasks:**

1. **Multiclass Classification**
   - Uses all three Iris flower classes.
   - Uses petal length and petal width for decision boundary visualization.
   - Applies the One-vs-Rest (`ovr`) decision function strategy.

2. **Binary Classification**
   - Uses Setosa and Versicolor classes.
   - Removes Virginica using conditional filtering.
   - Uses sepal length and sepal width for 2D visualization.

3. **SVM Classification with CSV Dataset**
   - Loads `Iris.csv`.
   - Uses all four flower measurement features.
   - Predicts the three Iris species.

## 🧠 Key Concepts Covered

### 1. Support Vector Machine (SVM)

- Understanding the Support Vector Machine algorithm.
- Learning how SVM finds an optimal decision boundary (hyperplane).
- Understanding how SVM separates different classes.
- Learning the role of support vectors.
- Understanding how SVM can be used for binary and multiclass classification.

### 2. Iris Dataset

- Loading the Iris dataset using `load_iris()`.
- Loading an external dataset using `pd.read_csv()`.
- Selecting flower measurement features.
- Understanding the three Iris flower species.
- Working with binary and multiclass classification.

### 3. Binary Classification

- Selecting only Setosa and Versicolor classes.
- Removing Virginica using conditional filtering.
- Training an SVM model using two classes.
- Understanding how SVM separates two categories.

### 4. Multiclass Classification

- Using all three Iris flower classes.
- Training SVM to classify Setosa, Versicolor, and Virginica.
- Using `decision_function_shape='ovr'`.
- Understanding the One-vs-Rest classification strategy.

### 5. Train-Test Split

- Splitting the dataset using `train_test_split()`.
- Using 80% data for training and 20% for testing.
- Setting `random_state=42` for reproducibility.
- Testing different random states from 1 to 100.
- Understanding how different data splits can affect model accuracy.

### 6. Support Vector Classifier

- Initializing the model using `SVC()`.
- Understanding the role of the SVC classifier.
- Using `kernel='linear'` for linear decision boundaries.
- Training the model using `fit()`.

### 7. Feature Scaling

- Understanding the importance of feature scaling in SVM.
- Applying `StandardScaler()` to standardize input features.
- Transforming features to have approximately zero mean and unit variance.
- Understanding how scaling helps SVM work with features having different ranges.

### 8. Decision Boundary Visualization

- Creating a custom `plot_decision_boundary()` function.
- Generating a mesh grid using `np.meshgrid()`.
- Creating coordinate points using `np.linspace()`.
- Predicting class labels across the mesh grid.
- Visualizing decision regions using `plt.contourf()`.
- Displaying flower samples using `plt.scatter()`.
- Understanding how SVM separates different classes visually.

### 9. Model Evaluation

- Predicting test data using `predict()`.
- Calculating accuracy using `accuracy_score()`.
- Generating a classification report using `classification_report()`.
- Creating a confusion matrix using `confusion_matrix()`.
- Understanding precision, recall, and F1-score.

### 10. Random State Experimentation

- Running the SVM model with random states from 1 to 100.
- Using different training and testing splits.
- Calculating accuracy for every random state.
- Understanding how data splitting influences model performance.

## 🛠️ Tech Stack

- **Python** – Programming language
- **NumPy** – Numerical operations and array manipulation
- **Pandas** – Data loading and manipulation
- **Matplotlib** – Decision boundary visualization
- **Scikit-learn** – Machine learning implementation
- **SVC** – Support Vector Machine classifier
- **StandardScaler** – Feature scaling
- **Jupyter Notebook** – Writing and executing Python code

## 📈 Machine Learning Operations Performed

| Operation | Function / Class | Purpose |
|---|---|---|
| Dataset Loading | `pd.read_csv()` | Loads the Iris CSV dataset |
| Built-in Dataset Loading | `datasets.load_iris()` | Loads the Scikit-learn Iris dataset |
| Feature Selection | `df[[...]]` | Selects input features |
| Target Selection | `df['Species']` | Selects the target variable |
| Data Filtering | `X[y != 2]` | Removes the third class for binary classification |
| Data Splitting | `train_test_split()` | Splits data into training and testing sets |
| Model Initialization | `SVC()` | Creates the SVM classifier |
| Feature Scaling | `StandardScaler()` | Standardizes input features |
| Model Training | `fit()` | Trains the SVM classifier |
| Prediction | `predict()` | Predicts flower species |
| Accuracy Evaluation | `accuracy_score()` | Calculates classification accuracy |
| Classification Report | `classification_report()` | Evaluates precision, recall, and F1-score |
| Confusion Matrix | `confusion_matrix()` | Displays correct and incorrect predictions |
| Mesh Grid Creation | `np.meshgrid()` | Creates coordinate points for decision boundary visualization |
| Coordinate Generation | `np.linspace()` | Generates evenly spaced values |
| Decision Boundary | `plt.contourf()` | Visualizes classification regions |
| Scatter Plot | `plt.scatter()` | Displays flower samples |
| Random State Experiment | `range(1, 101)` | Tests model accuracy with 100 random states |

## 💡 Key Learnings

1. Learned the fundamentals of the Support Vector Machine algorithm.
2. Understood how SVM creates decision boundaries to separate classes.
3. Practiced binary and multiclass classification.
4. Learned the importance of support vectors and hyperplanes.
5. Understood the role of different kernel functions.
6. Practiced feature scaling using StandardScaler.
7. Learned how to visualize SVM decision boundaries.
8. Understood the One-vs-Rest strategy for multiclass classification.
9. Evaluated model performance using accuracy, classification reports, and confusion matrices.
10. Learned how different random states affect model accuracy.
11. Practiced creating custom visualization functions using Matplotlib.
12. Understood how SVM can be applied to classification problems.

## 📁 Project Structure

```
SVM_Iris_Classification
│
├── Iris.csv
├── SVM_Classification.ipynb
└── README.md
```

## 🚀 Future Improvements

- Compare different SVM kernels such as Linear, Polynomial, RBF, and Sigmoid.
- Experiment with different values of `C` and `gamma`.
- Apply GridSearchCV for hyperparameter tuning.
- Compare SVM performance with Logistic Regression, KNN, and Decision Tree.
- Visualize support vectors and optimal hyperplanes.
- Use cross-validation to evaluate model performance.
- Compare binary and multiclass classification results.
- Apply SVM to other real-world classification datasets.