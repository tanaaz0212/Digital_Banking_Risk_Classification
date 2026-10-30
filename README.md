# Digital Banking Risk Classification

## Project Overview

The Digital Banking Risk Classification project uses machine learning to classify banking records into low-risk and high-risk categories.

The main objective of this project is to identify high-risk cases and understand how machine learning can help in banking risk management.

The target variable is `risk_status`:

- `0` = Low Risk
- `1` = High Risk

Since the dataset contains more low-risk cases than high-risk cases, different techniques are used to handle class imbalance and improve model performance.

## Dataset Information

- **Dataset Name:** Risk_Alert_Classifier_Dataset_4600.csv
- **Total Records:** 4,600
- **Total Columns:** 19
- **Target Variable:** risk_status

The dataset is explored to understand its structure, data types, missing values, duplicate records, and class distribution.

## Project Objectives

The main objectives of this project are:

- To understand and analyze the banking risk dataset.
- To perform data preprocessing and handle missing values.
- To identify class imbalance in the dataset.
- To build classification models.
- To apply sampling techniques to handle imbalanced data.
- To evaluate and compare model performance.
- To identify the best-performing model for risk classification.

## Technologies and Libraries Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn

## Project Workflow

### 1. Data Loading and Understanding

The dataset is loaded using Pandas.

The following functions are used to understand the data:

- `head()`
- `info()`
- `describe()`
- `isna().sum()`
- `duplicated().sum()`

### 2. Data Preprocessing

The data is prepared before applying machine learning models.

The preprocessing steps include:

- Checking and removing duplicate records.
- Checking missing values.
- Separating independent and dependent variables.
- Encoding categorical variables.
- Handling missing values using KNN Imputation.
- Splitting the dataset into training and testing sets using stratified sampling.

### 3. Logistic Regression

Logistic Regression is used as the baseline classification model.

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC

### 4. Handling Class Imbalance

The dataset contains an imbalance between low-risk and high-risk cases.

The following sampling techniques are applied to the training data:

- Random Under-Sampling
- Random Over-Sampling
- SMOTE
- ADASYN

The performance of these techniques is compared using classification metrics.

### 5. Decision Tree and Random Forest

Decision Tree and Random Forest classifiers are trained to improve classification performance.

Random Forest combines multiple decision trees to make predictions and can provide better stability than a single decision tree.

### 6. Hyperparameter Tuning

RandomizedSearchCV is used to find suitable Random Forest hyperparameters.

Cross-validation is used to evaluate different parameter combinations.

Recall is considered during tuning because identifying high-risk cases is important in this project.

### 7. Model Evaluation and Comparison

The models are compared using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

ROC curves are also plotted to compare the ability of the models to distinguish between low-risk and high-risk cases.

## Evaluation Metrics

**Accuracy:** Measures the overall percentage of correct predictions.

**Precision:** Measures how many predicted high-risk cases are actually high-risk.

**Recall:** Measures how many actual high-risk cases are correctly identified.

**F1 Score:** Represents the balance between Precision and Recall.

**ROC-AUC:** Measures the ability of the model to distinguish between the two classes.

**Confusion Matrix:** Shows the number of correct and incorrect predictions.

Recall is especially important because a false negative means that an actual high-risk case was classified as low-risk.

## Models Used

The following machine learning models are used in this project:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Tuned Random Forest Classifier

## Results

The performance of the models is compared using classification metrics.

The final model is selected based on its ability to identify high-risk cases while maintaining a reasonable precision score.

The final model name and evaluation scores are reported after executing the notebook.

## Conclusion

The Digital Banking Risk Classification project demonstrates the use of machine learning for identifying low-risk and high-risk banking records.

The dataset is explored and preprocessed before training the models. Logistic Regression is used as a baseline model, while Decision Tree and Random Forest classifiers are also trained and evaluated.

Different sampling techniques, including Under-Sampling, Over-Sampling, SMOTE, and ADASYN, are applied to handle class imbalance.

The models are compared using Accuracy, Precision, Recall, F1 Score, ROC-AUC, and Confusion Matrix.

Recall is given special importance because identifying actual high-risk cases is an important objective in banking risk classification.

This project demonstrates how machine learning can support banking risk analysis and help in making better risk management decisions.

## How to Run the Project

1. Download or clone this repository.
2. Install the required Python libraries.
3. Place the dataset file in the same folder as the Jupyter Notebook.
4. Open the notebook in Jupyter Notebook or JupyterLab.
5. Run all cells from top to bottom.
6. Review the model comparison table, evaluation metrics, and plots.

## Project Files

- `Digital_Banking_Risk_Classification.ipynb` — Jupyter Notebook containing the complete project.
- `Risk_Alert_Classifier_Dataset_4600.csv` — Dataset used for analysis and modelling.
- `Digital_Banking_Risk_Classification_Theory.docx` — Theory and project report.
- `README.md` — Project description and instructions.
- `digital_banking_risk_model.pkl` — Saved model, if generated.
