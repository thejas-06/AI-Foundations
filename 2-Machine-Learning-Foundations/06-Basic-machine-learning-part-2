# Machine Learning Workflow with Standardization and Evaluation - Learning Notes  

## Overview  
In this lesson, we extend the previous demo by incorporating additional steps into the machine learning workflow. The demo covers duplicating and renaming notebooks, importing required libraries, understanding **standardization**, splitting datasets into training and testing sets, training a **logistic regression model**, evaluating the model using **accuracy score**, and making predictions on **new unseen data**.  

---

## Key Concepts  
- **NumPy**: A Python library used for numerical computations and provides arrays and mathematical functions.  
- **Train Test Split**: Function from scikit-learn to split datasets into training and testing sets.  
- **StandardScaler**: Class from scikit-learn used to standardize features to have mean 0 and standard deviation 1.  
- **Accuracy Score**: Function from scikit-learn metrics module used to calculate model prediction accuracy.  
- **Standardization**: Ensures all features are on the same scale, preventing larger magnitude features from dominating.  
- **Random State**: Parameter to make dataset splits reproducible across runs.  
- **Model Training**: Teaching the model the relationship between features and labels.  
- **Evaluation**: Measuring how well the model performs on unseen test data.  
- **Prediction on New Data**: Using trained models to classify new, unseen examples.  

---

## Detailed Notes    

### Library Imports  
```python
# Import necessary libraries
import pandas as pd
from sklearn.linear_model import LogisticRegression
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score

# Loading the data set and displaying the first few rows
df = pd.read_csv('Iris.csv')
df.head()

# Split the data into features X and labels y
x = df.drop(columns=["Id","Species"])
y = df["Species"]

# Split the data into training and testing set
X_train, X_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=42)

# Standardize the features
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# Create a machine learning model
model = LogisticRegression()
model.fit(X_train, y_train)

# Evaluate the model on testing set
y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

# Sample new data for prediction
new_data = np.array([[4.6,3.5,1.5,0.2],
                     [5.1,3.5,1.4,0.2],
                     [6.3,2.9,1.4,0.3]])

# Standardize the new data
new_data_scaled = scaler.transform(new_data)

# Make predictions
predictions = model.predict(new_data_scaled)

# Display the predicted classes
print("Predicted classes:", predictions)
# Example Output: ['Iris-setosa' 'Iris-setosa' 'Iris-versicolor']

```
# Extended Machine Learning Workflow - Logistic Regression (Iris Dataset)

## Standardization  
Process of transforming data so it has mean of 0 and standard deviation of 1.  
Important because it ensures all features are treated equally by the model.  

**Example:**  
- Features: square footage (1000–5000) vs. bedrooms (1–6).  
- Without scaling, square footage dominates the model.  
- Standardization ensures both are on comparable scales.  

---

## Train-Test Split  
Divides data into:  
- `X_train`, `X_test` (features)  
- `y_train`, `y_test` (labels)  

The `random_state` parameter ensures reproducibility.  
**Example:** setting `random_state=42` gives the same split each time.  

---

## Model Training  
- Create a logistic regression model instance.  
- Train on standardized training features (`X_train_scaled`) and training labels (`y_train`).  
- The model learns patterns from the training data.  

---

## Evaluation  
- Use the trained model to predict on `X_test_scaled`.  
- Compare predicted labels with true labels (`y_test`).  
- **Accuracy score** = number of correct predictions / total predictions.  

In this demo, accuracy = **1 (100%)**.  

---

## Prediction on New Data  
- Create sample new data using NumPy.  
- Represents attributes of iris flowers:  
  - Sepal length  
  - Sepal width  
  - Petal length  
  - Petal width  
- Standardize new data using `StandardScaler` (same as training/testing data).  
- Use trained model to predict species of new iris samples.  

**Predicted Classes:**  
- First sample → *Iris-setosa*  
- Second sample → *Iris-virginica*  
- Third sample → *Iris-setosa*  

---

## Important Terms  
- **NumPy**: Library for numerical computations and arrays.  
- **Train Test Split**: Function to divide dataset into training and test subsets.  
- **StandardScaler**: Scales features to mean 0 and standard deviation 1.  
- **Accuracy Score**: Metric to measure ratio of correct predictions.  
- **Standardization**: Rescaling process to ensure features are comparable.  
- **Random State**: Controls randomness for reproducible dataset splitting.  
- **Model Training**: Teaching the model to map features to labels.  
- **Evaluation**: Testing model on unseen data to check performance.  
- **Overfitting**: When a model performs well on training data but poorly on unseen data.  

---

## Summary  
In this extended demo, we:  
- Imported essential libraries (`NumPy`, `train_test_split`, `StandardScaler`, `accuracy_score`).  
- Standardized dataset features for consistent scaling.  
- Split data into training and testing sets with reproducibility using `random_state`.  
- Trained a logistic regression model on standardized training data.  
- Evaluated the model with accuracy score, achieving **100% accuracy**.  
- Created and standardized new data samples.  
- Used the trained model to predict iris flower species from new attributes.  

