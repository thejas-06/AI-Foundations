# Demonstration: Deep Learning for Separating Complex Data Points - Learning Notes

## Overview
In this demonstration, we explore how **deep learning** can be applied to separate a complex set of data points. The dataset is created using the **make_circles** function from the sklearn library, and we observe how classifiers, particularly **Multilayer Perceptrons (MLP)**, learn to classify circular data distributions.

## Key Concepts
- **make_circles dataset**: Generates concentric circles with labels 0 and 1.
- **Parameters of make_circles**:
  - `n_samples`: Total number of data points.
  - `noise`: Randomness added to the data.
  - `factor`: Controls distance between the circles.
  - `random_state`: Seed for reproducibility.
- **Multilayer Perceptron (MLP)**:
  - Consists of hidden layers with neurons.
  - More neurons = more complex and accurate decision boundaries.
- **Interactive widget**: Adjusts hidden layer size dynamically.
- **update_plot function**: Handles dataset creation, training, prediction, and visualization of decision boundaries.

## Detailed Notes

### Dataset Creation
- **make_circles** is used to create data points.
- An **outer circle** is generated with label `0`.
- An **inner circle** is generated with label `1`.
- Goal: Train a classifier to correctly separate these sets of data points.
- Example:
  - A point created in the inner region should be classified as `1`.
  - A point created in the outer region should be classified as `0`.

### Parameters of `make_circles`
- `n_samples = 300`: Produces 300 data points.
  - 150 red (label 0)
  - 150 green (label 1)
- `noise`: Adds randomness to data generation.
- `factor = 0.5`: Controls spacing between circles.
- `random_state`: Acts as a seed to reproduce data points.

#### Parameter Experiments
- Reducing `n_samples` → fewer data points.
- Increasing `noise` → distribution becomes more random.
- Adjusting `factor` (e.g., 0.7) → reduces distance between concentric circles.

### Classifier Behavior
- **MLP with hidden layers**:
  - **1 neuron**: Predicts all points as class 0 → poor performance.
  - **2 neurons**: Some points classified correctly, but errors remain.
  - **3 neurons**: More complex boundary, better accuracy.
  - **4 neurons**: Decision boundary becomes more complex, improves accuracy.
  - **5–6 neurons**: Increasingly complex and accurate decision boundaries.

### Code Walkthrough
- **Hidden layer size slider**:
  - Implemented with an **interactive widget**.
  - Calls a function whenever slider value changes.
  - Passes updated hidden layer size to the function.

- **update_plot function**:
  - Dataset: Array of data points with x, y coordinates and labels (0 or 1).
  - **MLPClassifier**:
    - One layer with multiple neurons.
    - Activation function: **ReLU** (non-linear boundaries).
    - Trains until **maximum iterations** are reached.
    - `random_state` initializes weights and biases.
  - **Training**:
    - Classifier is trained on dataset.
  - **Prediction**:
    - Generate 100 x and y coordinates in the training range.
    - Reshape into **100 × 100 grid**.
    - Combine into new data points for prediction.
    - Reshape predicted labels for **decision boundary plotting**.
    - Predict labels for training data points to display with boundary.

- **Visualization**:
  - `contourf` plots decision boundary (separating labels 0 and 1).
  - Points plotted:
    - Label 0 → red
    - Label 1 → green
  - X and Y labels, title, and plot are displayed.

## Important Terms
- **make_circles**: Function to generate concentric circle datasets.
- **n_samples**: Total number of data points.
- **noise**: Random variation in dataset.
- **factor**: Controls spacing between concentric circles.
- **random_state**: Seed for reproducibility.
- **Multilayer Perceptron (MLP)**: Neural network with hidden layers and neurons.
- **ReLU activation function**: Non-linear activation used in MLP.
- **Decision boundary**: Region separating different predicted classes.
- **contourf**: Function to plot decision boundaries.

## Summary
- Deep learning effectively separates complex datasets like concentric circles.
- **make_circles** generates synthetic datasets with adjustable parameters (`n_samples`, `noise`, `factor`, `random_state`).
- **Multilayer Perceptron (MLP)** classifiers improve accuracy as the number of neurons increases, leading to more complex decision boundaries.
- **update_plot function** and **interactive widgets** allow dynamic visualization of classifier performance.
- Visualization with **contourf** clearly shows how points with labels `0` and `1` are separated by learned boundaries.
