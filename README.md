# Airline Passenger Satisfaction Prediction

An end-to-end machine learning project that predicts whether airline passengers are satisfied or neutral/dissatisfied based on demographic, travel, delay, and service-experience features.

## Project Overview

This project analyzes airline passenger satisfaction using machine learning techniques. The goal is to identify the factors that most influence passenger satisfaction and build a classification model that predicts whether a passenger is satisfied or neutral/dissatisfied.

The dataset contains 103,904 passenger records and includes demographic information, travel characteristics, delay information, and service ratings.

The project covers the complete machine learning workflow, including data preprocessing, exploratory data analysis, model development, model comparison, hyperparameter tuning, cross-validation, final evaluation, feature importance analysis, PCA visualization, and ethical considerations.

## Dataset

**Dataset:** Airline Passenger Satisfaction  
**Source:** Kaggle  
**Problem Type:** Binary Classification  
**Target Variable:** `satisfaction`

Dataset source:

https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

The dataset files are not included in this repository.

After downloading the dataset, place the files inside the `data` folder:

```text
data/train.csv
data/test.csv
```

## Project Workflow

- Data loading and inspection
- Exploratory data analysis
- Missing-value analysis
- Data preprocessing
- Identifier-column removal
- Train/validation/test splitting
- Numerical feature imputation
- Feature standardization
- Categorical feature imputation
- One-hot encoding
- Logistic Regression baseline model
- Random Forest model
- Random Forest hyperparameter tuning
- Stratified 5-fold cross-validation
- Model comparison
- Precision, recall, F1-score, and ROC-AUC evaluation
- Final held-out test-set evaluation
- Feature importance analysis
- Principal Component Analysis
- Ethical considerations

## Technologies Used

- Python
- Pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Models Evaluated

The following machine learning models were evaluated:

- Logistic Regression
- Random Forest
- Tuned Random Forest

Logistic Regression was used as the baseline model. Random Forest was then evaluated as a nonlinear model, followed by hyperparameter tuning using RandomizedSearchCV and stratified cross-validation.

## Final Model Performance

The Tuned Random Forest achieved:

- **Accuracy:** 96.49%
- **F1-score:** 0.9590
- **ROC-AUC:** 0.9949

The final model was evaluated on a held-out test set that was not used during model training, model comparison, or hyperparameter tuning.

## Key Findings

Feature importance analysis showed that several passenger-experience variables were strong predictors of satisfaction, including:

- Online boarding
- Inflight Wi-Fi service
- Cabin class
- Type of travel
- Inflight entertainment
- Seat comfort

These results represent predictive relationships in the model and should not be interpreted as causal relationships.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix
- Stratified 5-fold cross-validation

The validation set was used for model comparison and selection, while the held-out test set was reserved for the final Tuned Random Forest evaluation.

## Feature Importance

Feature importance from the Tuned Random Forest was used to understand which variables contributed most strongly to model predictions.

The feature importance analysis provides insight into model behavior but does not establish that a particular feature directly causes passenger satisfaction or dissatisfaction.

## Principal Component Analysis

Principal Component Analysis was used to examine the dimensional structure of the preprocessed dataset.

The project evaluates cumulative explained variance and includes a two-dimensional PCA visualization of the training data.

PCA was used for exploratory analysis and visualization and was not used to train the final Random Forest model.

## Ethical Considerations

The project considers potential issues related to:

- Dataset bias
- Model transparency
- False positive and false negative predictions
- Differences in performance across passenger groups
- Responsible use of model predictions

The model is intended to support passenger-experience analysis and should not replace human judgment or direct passenger feedback.

## Repository Structure

```text
Airline_Passenger_Satisfaction_Prediction/
├── Airline_Passenger_Satisfaction_Prediction.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    ├── train.csv
    └── test.csv
```

The CSV files inside the `data` folder are stored locally and excluded from Git tracking.

## Installation

Clone the repository:

```bash
git clone https://github.com/rishithaaaa-2703/Airline_Passenger_Satisfaction_Prediction.git
```

Move into the repository:

```bash
cd Airline_Passenger_Satisfaction_Prediction
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Download the Airline Passenger Satisfaction dataset from Kaggle and place `train.csv` and `test.csv` inside the `data` folder.

## Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Airline_Passenger_Satisfaction_Prediction.ipynb
```

Run the notebook cells from top to bottom.

## Requirements

The project uses the following Python libraries:

```text
numpy
pandas
seaborn
matplotlib
scikit-learn
jupyter
```
