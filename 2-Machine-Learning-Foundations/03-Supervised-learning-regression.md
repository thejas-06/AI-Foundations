# Supervised Learning - Linear Regression (Learning Notes)

## Overview
This lesson focuses on **supervised learning** with a detailed explanation of **linear regression**. It explains how supervised learning works using labeled data, explores real-world applications, and demonstrates how regression can be used for tasks like predicting house prices.

## Key Concepts
- **Supervised Learning**: A machine learning model that learns from labeled data by mapping input to output.
- **Applications**:
  - House price prediction
  - Cancer detection
  - Sentiment analysis
  - Stock price prediction
- **Input and Output Mapping**: The model learns the relationship between input data and corresponding target values.
- **Regression vs. Classification**:
  - Regression → Continuous outputs
  - Classification → Categorical outputs
- **Linear Regression**: Predicts continuous outcomes by fitting a straight line through data points.
- **Training Data**: Consists of input-output pairs used to train the model.
- **Loss/Error**: The difference between actual and predicted values, minimized during training.

## Detailed Notes  

### Introduction to Supervised Learning
- Supervised learning is a machine learning model that **learns from labeled data**.  
- The model learns the mapping between the **input** and the **output**.  
- Typical applications include:
  - Predicting house prices using house size
  - Detecting cancer (malignant or not) using medical details
  - Sentiment analysis of customer reviews
  - Stock price prediction using market data  

### Input and Output Mapping
- Supervised learning involves **teaching a model the relationship** between input and output.  
- The process is similar to a teacher instructing a student:
  - The model is trained with past outcomes
  - It learns the mapping between input and output  

### Types of Outputs
- **Continuous output** → use **Regression**  
- **Categorical output** → use **Classification**  

### Example: House Price Prediction
- Goal: Predict house price based on **house size (square feet)**.  
- **Independent Feature (Input)**: House size  
- **Dependent Feature (Output)**: House price  
- A single row of input and output is a **training example (tuple)**.  
- The dataset is plotted as a scatter plot:
  - As house size increases, price also increases
  - A straight line can represent this relationship  

### Linear Regression Model
- The relationship between input and output is expressed with a line.  
- **Equation**:  
  \[
  f(x) = w \times x + b
  \]  
  - **w** → slope (rate of change of price with respect to size)  
  - **b** → bias (y-intercept)  
- Adjusting **slope** and **bias** moves or tilts the line to best fit the data.  

### Training Process
- The algorithm iteratively adjusts **weights (w)** and **bias (b)** to minimize error.  
- **Error**: Difference between actual and predicted values.  
- **Loss**: Penalty for a bad prediction.  
  - Perfect prediction → loss = 0  
  - Otherwise → loss is higher  
- One common method: Square the difference between actual and predicted values.  

### Outcome
- Once the model finds optimal **w** and **b**, the line can predict unseen data.  
- Example: Predicting the price of a house of size **1,100 sq ft** using the trained line.  

## Important Terms
- **Supervised Learning**: Model trained with labeled data to map input to output.  
- **Independent Feature**: Input variable (e.g., house size).  
- **Dependent Feature**: Output variable (e.g., house price).  
- **Training Example / Tuple**: A single input-output data pair.  
- **Error**: Difference between predicted and actual values.  
- **Loss**: Penalty measure for prediction error.  
- **Slope (w)**: Rate of change in output with respect to input.  
- **Bias (b)**: The y-intercept of the regression line.  

## Summary
- Supervised learning uses labeled data to learn input-output mappings.  
- Outputs can be **continuous** (regression) or **categorical** (classification).  
- Linear regression predicts continuous outcomes using a line.  
- The model adjusts slope and bias iteratively to minimize loss.  
- Training involves reducing error until the model can accurately predict outcomes, such as **house price prediction**.  
