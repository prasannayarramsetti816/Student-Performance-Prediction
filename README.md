# Student Performance Prediction Using Machine Learning

## Project Overview

This project uses Machine Learning to predict whether a student will Pass or Fail based on study habits, attendance, previous marks, assignment scores, sleep hours, participation, and subject average.

The project uses a synthetic dataset containing 500 student records for learning and educational purposes.

## Objectives

- Analyze student performance data.
- Check missing values and duplicate records.
- Prepare features and target variables.
- Apply feature scaling using StandardScaler.
- Train a Logistic Regression classification model.
- Evaluate model performance using accuracy, confusion matrix, precision, recall, and F1-score.
- Visualize the relationship between study hours and student results.
- Predict the result for a new student record.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset Description

The dataset contains 500 records and 8 columns, including 7 input features and 1 target variable.

| Feature | Description |
|---|---|
| Study_Hours | Hours spent studying |
| Attendance | Student attendance score |
| Previous_Marks | Previously obtained marks |
| Assignment_Score | Assignment performance score |
| Sleep_Hours | Hours of sleep |
| Participation | Classroom participation score |
| Subject_Average | Average subject score |
| Result | Target variable: Pass or Fail |

The target variable is encoded as:

- Fail = 0
- Pass = 1

## Project Workflow

1. Imported the required Python libraries.
2. Loaded and inspected the dataset.
3. Checked missing values and duplicate records.
4. Analyzed the distribution of Pass and Fail results.
5. Separated input features and the target variable.
6. Encoded the target variable into numerical values.
7. Split the dataset into training and testing sets using an 80:20 ratio.
8. Applied StandardScaler to scale the input features.
9. Trained a Logistic Regression model.
10. Generated predictions using the test dataset.
11. Evaluated the model using accuracy, confusion matrix, and classification report.
12. Predicted the result for a new student record.
13. Created a box plot to compare study hours for students who passed and failed.

## Machine Learning Algorithm

**Logistic Regression**

Logistic Regression is a supervised Machine Learning algorithm used for classification problems. In this project, it predicts one of two classes: Pass or Fail.

## Model Evaluation

The model achieved the following results on the test dataset:

- Algorithm: Logistic Regression
- Training records: 400
- Testing records: 100
- Test accuracy: 91%

### Confusion Matrix

```text
[[37  7]
 [ 2 54]]
```

The confusion matrix represents:

- 37 Fail records correctly predicted as Fail.
- 7 Fail records incorrectly predicted as Pass.
- 2 Pass records incorrectly predicted as Fail.
- 54 Pass records correctly predicted as Pass.

### Classification Report

| Metric | Fail | Pass |
|---|---:|---:|
| Precision | 0.95 | 0.89 |
| Recall | 0.84 | 0.96 |
| F1-score | 0.89 | 0.92 |

Overall test accuracy: **91%**

These results correspond to the current train-test split and may vary if the dataset or model settings change.

## Sample Prediction

The model was tested with a sample student record containing the following values:

- Study Hours: 6
- Attendance: 85
- Previous Marks: 75
- Assignment Score: 80
- Sleep Hours: 7
- Participation: 70
- Subject Average: 78

**Predicted Result: Pass**

## Data Visualization

A box plot created using Seaborn and Matplotlib compares the distribution of study hours between students who passed and students who failed.

This visualization helps explore patterns in study hours across the two result groups.

## How to Run the Project

### 1. Install the Required Libraries

Run the following command in your terminal or Jupyter environment:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 2. Download the Project Files

Download the Jupyter Notebook and CSV dataset from this repository.

### 3. Update the Dataset Path

Ensure that the CSV file path in the notebook points to the correct location on your computer. If both files are in the same folder, you can use:

```python
df = pd.read_csv("Student_Performance.csv")
```

### 4. Run the Notebook

Open the notebook in Jupyter Notebook and run all cells in order.

## Limitations

- The dataset is synthetic and is intended for educational and practice purposes.
- The model learns patterns from the supplied dataset and may not generalize to real-world student data.
- Accuracy alone does not establish that a model is suitable for real educational decisions.
- The predictions should not be used as the sole basis for evaluating actual students.

## Future Improvements

- Compare Logistic Regression with other classification algorithms.
- Perform cross-validation and hyperparameter tuning.
- Evaluate additional metrics and feature importance.
- Test the model on a suitable real-world dataset, if available.
- Develop an interactive application for entering student details and viewing predictions.

## Author

Yarramsetti Lakshmi Prasanna

Created as a Machine Learning practice project to demonstrate data preprocessing, feature scaling, classification, model evaluation, and visualization.
