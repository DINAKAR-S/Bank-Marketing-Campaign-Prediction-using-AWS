# 🏦 Bank Marketing Campaign Prediction using Amazon SageMaker and XGBoost

This project demonstrates how to build, train, deploy, and evaluate a machine learning model using **AWS SageMaker**. The goal is to predict whether a bank customer will subscribe to a term deposit based on historical marketing data.

---

## 📊 Project Overview

- **Problem**: Predict customer subscription to a term deposit
- **Algorithm**: XGBoost (SageMaker built-in)
- **Cloud Platform**: AWS (SageMaker, S3, IAM)
- **Deployment**: Real-time SageMaker endpoint
- **Evaluation**: Confusion Matrix & Accuracy Score

---

## 🧰 Tools & Services Used

| Service/Tool        | Purpose                          |
|---------------------|----------------------------------|
| Amazon SageMaker    | Notebook, training, deployment   |
| Amazon S3           | Data storage                     |
| IAM Role            | Permission control               |
| XGBoost             | ML algorithm                     |
| Pandas / NumPy      | Data preprocessing               |
| SageMaker SDK       | Model orchestration              |

---

## 🧪 Dataset

- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
- Pre-cleaned dataset provided by AWS
- Features: Age, job, marital status, education, previous contacts, etc.
- Target: `y_yes` (1 if customer subscribed, 0 otherwise)

---

## 🛠️ Workflow

### 1. **Setup Environment**
- Created a SageMaker notebook instance
- Created a unique S3 bucket for the project

### 2. **Load & Prepare Data**
- Loaded pre-cleaned CSV dataset
- Performed 70/30 train-test split
- Reordered columns (label first), removed headers
- Uploaded `train.csv` and `test.csv` to S3

### 3. **Train Model Using XGBoost**
- Used SageMaker's built-in XGBoost container
- Set hyperparameters (`max_depth`, `eta`, `gamma`, etc.)
- Initiated training with `estimator.fit()`

### 4. **Deploy Model**
- Deployed trained model as a real-time endpoint
- Configured endpoint to accept CSV input

### 5. **Make Predictions**
- Sent test data to endpoint
- Collected and parsed prediction results
- Evaluated model using a confusion matrix

### 6. **Cleanup**
- Deleted deployed endpoint
- Cleared S3 data to avoid AWS charges

---

## 📈 Results

- Model trained successfully on SageMaker
- Deployed as a live endpoint
- Predictions matched expected shape and logic
- Confusion matrix showed reasonable classification accuracy

---

## 💡 What I Learned

- End-to-end machine learning pipeline on AWS
- Working with SageMaker Estimators and built-in algorithms
- Managing data in S3 and permissions with IAM roles
- Deploying models to real-time endpoints
- Evaluating classification models using real-world data

---
