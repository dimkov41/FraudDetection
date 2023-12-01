# Online Transaction Fraud Detection

## Data Description

The dataset contains information about online transactions and their characteristics. Each transaction is represented by a row in the dataset, with attributes such as step, type, amount, nameOrg, oldbalanceOrg, newbalanceOrg, nameDest, oldbalanceDest, newbalanceDest, and isFraud.

### Fields

- **step:**
  - Definition: Represents a unit of time in the real world, where each step corresponds to one hour.
  - Context: The simulation spans 30 days, and there are a total of 744 steps.

- **type:**
  - Definition: Denotes the type of transaction and can take values such as CASH-IN, CASH-OUT, DEBIT, PAYMENT, and TRANSFER.
  - Context: Describes the nature of the financial activity undertaken in each transaction.

- **amount:**
  - Definition: Signifies the monetary value of the transaction.
  - Context: Represents the amount of funds involved in each financial operation.

- **nameOrg:**
  - Definition: Identifies the customer initiating the transaction.
  - Context: Associates each transaction with the account holder responsible for its initiation.

- **oldbalanceOrg:**
  - Definition: Reflects the initial account balance of the customer before the transaction.
  - Context: Provides the starting financial position of the account holder.

- **newbalanceOrg:**
  - Definition: Indicates the new account balance of the customer after the transaction.
  - Context: Captures the updated financial status of the account holder following the transaction.

- **nameDest:**
  - Definition: Identifies the recipient customer of the transaction.
  - Context: Associates transactions with the account to which funds are being transferred.

- **oldbalanceDest:**
  - Definition: Represents the initial account balance of the recipient before the transaction. There is not information for customers that start with M (Merchants).
  - Context: Offers insight into the starting financial position of the recipient account.

- **newbalanceDest:**
  - Definition: Signifies the new account balance of the recipient after the transaction. There is not information for customers that start with M (Merchants).
  - Context: Captures the updated financial status of the recipient account following the transaction.

- **isFraud:**
  - Definition: Binary indicator (0 or 1) highlighting whether the transaction is fraudulent (1) or not (0).
  - Context: Identifies transactions involving fraudulent behavior within the simulation.

## Goal

The primary objective of this analysis is to develop a robust classification model that can accurately predict whether a given online transaction is fraudulent or not. Leveraging the features provided in the dataset, the goal is to train a machine learning model capable of distinguishing between legitimate and fraudulent transactions.

## Project Approach

### 1. Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) involves using statistical and graphical techniques to explore the dataset's characteristics, understand its underlying structure, and uncover patterns, trends, relationships, and potential outliers. EDA is crucial in gaining insights early in the data science or machine learning project.

### 2. Data Preprocessing

Address any missing or anomalous values in the dataset. Encode categorical variables, if necessary. Scale numerical features to ensure uniformity in their impact on the model.

### 3. Handling Imbalance

Implement techniques to address class imbalance, such as oversampling the minority class (fraudulent transactions) using methods like SMOTE or undersampling the majority class.

### 4. Model Selection

Experiment with different classification algorithms such as Logistic Regression, Random Forest, XGBoost, etc. Utilize appropriate evaluation metrics for imbalanced datasets, emphasizing metrics like precision, recall, F1-score, and ROC-AUC.

### 5. Hyperparameter Tuning

Conduct a systematic search for optimal hyperparameters using techniques like GridSearchCV or RandomizedSearchCV to improve model performance.

### 6. Model Evaluation

Evaluate the performance of the trained model on a separate test dataset. Assess the model's ability to correctly classify fraudulent transactions while minimizing false positives.

### 7. Interpretability and Explainability

Strive for a model that not only performs well but is also interpretable. Understand the importance of each feature in the decision-making process.

## How to Run This Project

1. Clone this repository:

```
   git clone {url}
```

2. Install the required dependencies:

```
pip install -r requirements.txt
```


Run the Jupyter notebooks or Python scripts in the specified order.

Requirements

    pandas==1.3.3
    matplotlib==3.4.3
    seaborn==0.11.2
    numpy==1.21.2
    xgboost==1.5.0
    scikit-learn==0.24.2
    imbalanced-learn==0.8.0


## LICENCE

### Copyright (c) 2023 Radostin Dimkov

#### This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/legalcode).