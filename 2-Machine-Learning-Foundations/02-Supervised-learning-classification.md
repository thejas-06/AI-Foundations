# Supervised Learning - Classification (Learning Notes)

## Overview
This lesson introduces **supervised learning** with a focus on **classification**.  
The video explains how classification differs from regression, provides examples of binary and multi-class classification, introduces **logistic regression**, and demonstrates its use with a **student pass/fail example** and the **Iris dataset**.

---

## Key Concepts

- **Supervised Learning Model**
  - Output can be either **categorical** or **continuous**.
  - **Continuous output → Regression**
  - **Categorical output → Classification**

- **Regression**
  - Predicts a numeric output.
  - Example: House price prediction.

- **Classification**
  - Predicts a category or label.
  - Example: Detecting spam emails.

- **Types of Classification**
  - **Binary Classification**: Two possible outcomes (e.g., spam vs not spam).
  - **Multi-class Classification**: More than two categories (e.g., sentiment prediction: positive, negative, neutral).

- **Logistic Regression**
  - Algorithm for classification.
  - Predicts **true or false** outcomes.
  - Uses **sigmoid function** to output probabilities.

- **Iris Dataset**
  - Standard dataset with **150 instances**.
  - **Three classes**: Iris-setosa, Iris-versicolor, Iris-virginica.
  - **Four features**: sepal length, sepal width, petal length, petal width.
  - A case of **multi-class classification**.

---

## Detailed Notes

### Supervised Learning
- A supervised machine learning model produces outputs that are:
  - **Continuous** → handled with regression.
  - **Categorical** → handled with classification.

### Regression vs Classification
- **Regression**: Used for predicting numeric outcomes (e.g., house price prediction).  
- **Classification**: Assigns a category or label to the outcome.  
  - Example: Detecting whether an email is spam (binary classification).  
  - Example: Sentiment prediction (positive, negative, neutral → multi-class classification).  

### What is Classification?
- Classification is a supervised learning technique.  
- It categorizes or assigns data points into **predefined classes or categories** based on their **features or attributes**.  
- A **classifier** is trained on a labeled dataset.  
- Example: Training a classifier to detect spam mail.  
  - Outcome is **binary**: spam or not spam.  

### Logistic Regression
- A simple machine learning algorithm used for classification.  
- Predicts whether something is **true or false**.  

#### Example: Pass/Fail Prediction
- **Input feature**: Hours of study (independent variable).  
- **Output**: Pass or Fail (binary).  
- Students are assigned to either:
  - **Pass class** (passed the test), or  
  - **Fail class** (failed the test).  

#### How Logistic Regression Works
- Unlike linear regression (which uses a straight line), logistic regression uses an **S-shaped curve** called the **sigmoid function**.  
- The **sigmoid function** takes any real-valued number and maps it to a range between **0 and 1**.  
- This makes it possible to interpret the output as a **probability**.  

#### Threshold
- Output probability is compared to a threshold (e.g., 0.5).  
  - If probability ≥ 0.5 → classified as **Pass**.  
  - If probability < 0.5 → classified as **Fail**.  

##### Example:
- Student studies 6 hours → 80% probability → **Pass**.  
- Student studies 4 hours → 20% probability → **Fail**.  

### Iris Dataset Demo
- Dataset with **150 samples** of iris flowers.  
- Classes: **Iris-setosa, Iris-versicolor, Iris-virginica**.  
- Features: **sepal length, sepal width, petal length, petal width**.  
- Since there are **3 classes**, this is a **multi-class classification problem**.  
- Logistic regression is used to classify flowers based on their features.  

---

## Important Terms

- **Supervised Learning**: Machine learning where models are trained on labeled datasets.  
- **Regression**: Predicting continuous/numeric outcomes.  
- **Classification**: Predicting categorical outcomes.  
- **Binary Classification**: Classification with two outcomes.  
- **Multi-class Classification**: Classification with more than two categories.  
- **Classifier**: An algorithm trained on labeled data to assign categories.  
- **Logistic Regression**: Classification algorithm that predicts probabilities and uses the sigmoid function.  
- **Sigmoid Function**: An S-shaped function that maps values to the range [0,1].  
- **Threshold**: The cutoff value (commonly 0.5) used to assign a class based on probability.  
- **Iris Dataset**: A dataset with 150 flower samples, 4 features, and 3 classes used for classification tasks.  

---

## Summary

- Supervised learning can have either **continuous outputs (regression)** or **categorical outputs (classification)**.  
- **Classification** assigns labels to data points and can be **binary** or **multi-class**.  
- **Logistic regression** is a key algorithm for classification and uses the **sigmoid function** to map outputs to probabilities.  
- **Thresholding** is applied to probabilities to decide the class.  
- The **Iris dataset** demonstrates **multi-class classification** with logistic regression.  

---
