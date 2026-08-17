# Student Performance & Backlog Prediction

## 📌 Project Overview

This project uses **Machine Learning** to predict the number of backlogs of students based on their academic performance and participation.

The project uses two classification algorithms:

* **K-Nearest Neighbors (KNN)**
* **Decision Tree Classifier**

The models are trained using student performance data and their accuracy is compared to identify the better-performing model.

---

## 🎯 Objective

The main objective of this project is to:

* Analyze student performance data.
* Predict the number of student backlogs.
* Apply Machine Learning classification algorithms.
* Compare the performance of KNN and Decision Tree.
* Evaluate models using accuracy, classification report, and confusion matrix.
* Predict the backlog of a new student based on their performance.

---

## 📊 Dataset

The project uses a CSV file named:

`student_performance_data.csv`

### Features Used

| Feature          | Description                   |
| ---------------- | ----------------------------- |
| Attendance       | Student attendance percentage |
| Assessment marks | Marks obtained in assessments |
| Assignment score | Assignment performance        |
| Study hours      | Average study hours           |
| Sem marks        | Semester marks                |
| Participation    | Participation percentage      |

### Target Variable

**`no.of backlog`**

This represents the number/class of backlogs associated with a student.

---

## 🛠️ Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## 🤖 Machine Learning Models

### 1. K-Nearest Neighbors (KNN)

KNN predicts the target class based on the nearest data points.

The project uses:

```python
KNeighborsClassifier(n_neighbors=5)
```

Feature scaling is performed using `StandardScaler` because KNN is distance-based.

---

### 2. Decision Tree

Decision Tree classifies students based on different performance features.

The model uses:

```python
DecisionTreeClassifier(
    criterion="gini",
    max_depth=4,
    random_state=42
)
```

The Decision Tree is also visualized using `plot_tree()`.

---

## 🔄 Data Preprocessing

The following preprocessing steps are performed:

1. Load the CSV dataset using Pandas.
2. Remove the `%` symbol from the Attendance column.
3. Convert Attendance values into numeric format.
4. Check for missing values.
5. Fill missing numeric values using the median.
6. Separate features (`X`) and target (`y`).
7. Split the data into training and testing sets.
8. Apply `StandardScaler` for KNN.

---

## 📈 Model Evaluation

The models are evaluated using:

### Accuracy

Accuracy measures the percentage of correctly predicted records.

```python
accuracy_score(y_test, y_pred)
```

### Classification Report

The classification report provides:

* Precision
* Recall
* F1-score
* Support

### Confusion Matrix

The confusion matrix shows the number of correct and incorrect predictions for each class.

---

## 🌳 Decision Tree Visualization

The project generates a visual representation of the Decision Tree to understand how the model makes predictions.

The tree is displayed with:

* Feature names
* Classes
* Decision rules
* Gini values

---

## 🔮 New Student Prediction

The project also predicts the number of backlogs for a new student using their:

* Attendance
* Assessment marks
* Assignment score
* Study hours
* Semester marks
* Participation

Example:

```python
new_student = pd.DataFrame({
    "Attendance": [85],
    "Assessment marks": [17],
    "Assignment score": [25],
    "Study hours": [4.5],
    "Sem marks": [78],
    "Participation": [85]
})
```

Both KNN and Decision Tree provide a predicted backlog class.

---

## 📁 Project Structure

```text
Student-Performance-Prediction/
│
├── student_performance_data.csv
├── student_performance.py
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Install Python

Make sure Python is installed on your system.

### 2. Install Required Libraries

Open the terminal and run:

```bash
pip install pandas matplotlib scikit-learn
```

### 3. Place the Dataset

Keep:

```text
student_performance_data.csv
```

in the same folder as the Python file.

### 4. Run the Program

```bash
python student_performance.py
```

---

## 📌 Expected Output

The program displays:

```text
Dataset Loaded Successfully!

KNN MODEL
Accuracy: ...

DECISION TREE MODEL
Accuracy: ...

MODEL COMPARISON

KNN Accuracy           : ...%
Decision Tree Accuracy : ...%

Best Model: ...
```

It also displays confusion matrices and a Decision Tree visualization.

---

## 🚀 Future Improvements

* Add more student records for better model performance.
* Try additional Machine Learning algorithms such as Logistic Regression, Random Forest, and SVM.
* Perform hyperparameter tuning.
* Add a graphical user interface.
* Create a web-based student prediction application.
* Improve class balancing if the backlog classes are imbalanced.

---

## 👩‍💻 Author

**Ruchira Kudke**

MCA — Artificial Intelligence & Data Science

---

## 📄 License

This project is created for **educational and academic purposes**.
