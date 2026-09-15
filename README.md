# Student Performance Prediction Using Machine Learning

## 📌 Project Overview

This project applies basic machine learning techniques to analyze student academic and behavioral data, build predictive models, evaluate their performance, and identify students who may be at academic risk.

The project uses student information such as study hours, attendance, sleep hours, assignment scores, previous scores, and extracurricular activities to predict student performance categories.

## 🎯 Project Objectives

### General Objective

To apply basic machine learning techniques to analyze student data, build predictive models, evaluate their performance, and interpret results to support early identification of academic risk.

### Specific Objectives

* Collect and describe a suitable student performance dataset.
* Clean and prepare the dataset for machine learning.
* Handle missing values and duplicate records.
* Encode categorical variables.
* Perform exploratory data analysis (EDA).
* Train and compare different supervised machine learning models.
* Apply K-Means clustering to identify natural student groupings.
* Evaluate model performance using accuracy, precision, recall, and F1-score.
* Interpret the results and provide practical recommendations.

## 📊 Dataset

The dataset contains **501 student records** and includes the following variables:

| Feature                | Description                                                    |
| ---------------------- | -------------------------------------------------------------- |
| `student_id`           | Unique identifier for each student                             |
| `hours_studied`        | Number of hours spent studying                                 |
| `attendance_percent`   | Student attendance percentage                                  |
| `sleep_hours`          | Average number of hours slept                                  |
| `assignment_score`     | Assignment performance score                                   |
| `previous_scores`      | Previous academic performance                                  |
| `extracurricular`      | Whether the student participates in extracurricular activities |
| `exam_score`           | Student exam score                                             |
| `performance_category` | Student's performance category                                 |

The dataset initially contained missing values in `sleep_hours` and `assignment_score`, as well as one duplicate row. Missing numerical values were handled using the median, and the duplicate row was removed.

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Inspected the dataset structure and statistical information.
3. Checked for missing values.
4. Checked for duplicate records.
5. Removed duplicate records.
6. Filled missing numerical values using their respective medians.
7. Converted the `extracurricular` categorical variable into numerical values:

   * `Yes` → `1`
   * `No` → `0`
8. Selected relevant features for machine learning.

The `student_id` column was excluded because it is only an identifier. The `exam_score` column was also excluded from prediction because the target `performance_category` was derived from it, and including it would cause data leakage.

## 🔍 Exploratory Data Analysis

Exploratory data analysis was performed to investigate patterns and relationships within the student data.

The analysis includes visualizations and statistical exploration of variables such as:

* Study hours
* Attendance
* Sleep hours
* Assignment scores
* Previous scores
* Exam scores
* Student performance categories
* Feature correlations

## 🤖 Machine Learning Models

### 1. Logistic Regression

Logistic Regression was used as one of the supervised classification models for predicting student performance categories.

### 2. Decision Tree

A Decision Tree Classifier was trained to classify students according to their predicted performance category. The tree structure was also visualized to help interpret the model.

### 3. Neural Network

A Multi-Layer Perceptron (MLP) classifier was used as a basic neural network model for student performance classification.

### 4. K-Means Clustering

K-Means was applied as an unsupervised learning technique to identify natural behavioral groupings among students.

## 📈 Model Evaluation

The classification models were evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**
* **Classification Report**

These metrics were used to compare the performance of the different supervised learning models.

## 🧪 Train-Test Split

The cleaned dataset was divided into:

* **80% training data**
* **20% testing data**

A stratified split with `random_state=42` was used to maintain the distribution of the performance categories between the training and testing sets. The resulting split contained **400 training records and 100 testing records**.

## 🛠️ Technologies and Libraries

The project was developed using Python and Jupyter Notebook.

### Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

### Scikit-learn Components

* `train_test_split`
* `LabelEncoder`
* `StandardScaler`
* `LogisticRegression`
* `DecisionTreeClassifier`
* `KMeans`
* `MLPClassifier`
* Classification and evaluation metrics

## 📁 Project Structure

```text
Student-Performance-Analysis/
│
├── student_performance.csv
├── Student Performance Analysis.ipynb
└── README.md
```

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Navigate into the project folder

```bash
cd Student-Performance-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open the project notebook and run the cells from beginning to end.

## 💡 Key Purpose

The main purpose of this project is to demonstrate how machine learning can be used to analyze student data and support the early identification of academic risk.

The results can potentially help educators and institutions identify patterns associated with student performance and provide appropriate academic support.

## ⚖️ Ethical Considerations

Student performance prediction should be used responsibly.

Machine learning predictions should **support human decision-making rather than replace it**. Student data should be handled with appropriate privacy protections, and predictions should not be used to unfairly label or discriminate against students.

## 👨‍💻 Author

**Wesley Junior**

Diploma in Artificial Intelligence and Cybersecurity

Africa International University
