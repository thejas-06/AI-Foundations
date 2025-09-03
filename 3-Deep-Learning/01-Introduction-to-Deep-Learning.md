# Deep Learning - Learning Notes

## Overview
In this lesson, we learn about **deep learning**, a subset of machine learning that focuses on training artificial neural networks (ANNs) to solve tasks such as image classification. The video explains how ANNs process raw data, extract patterns, and make predictions. It also covers the history of deep learning, applications across various data types, architectures suited for specific tasks, and the building blocks of ANNs, along with an example of handwritten digit recognition using backpropagation.

## Key Concepts
- **Deep Learning**: Subset of machine learning that uses ANNs to process raw data and predict outcomes.
- **Artificial Neural Network (ANN)**: Inspired by the human brain; consists of neurons, layers, weights, biases, and activation functions.
- **Automatic Feature Extraction**: Deep learning extracts features directly from data instead of requiring manual specification.
- **Parallel Computation**: Data is split into batches and processed in parallel, enabling scalability and performance.
- **History of Deep Learning**: Development timeline from the 1950s to modern-day applications like generative models.
- **Applications**: Image, text, and audio tasks with specific architectures suited for each.
- **Training with Backpropagation**: Adjusting weights iteratively using errors to improve ANN predictions.

## Detailed Notes

### What is Deep Learning?
- Subset of machine learning focused on training **artificial neural networks (ANNs)**.
- Example: **image classification** using handwritten digits.
- **ANNs**:
  - Accept raw inputs like image pixels.
  - Extract patterns (edges, curves, etc.).
  - Correlate patterns to predict outcomes (e.g., digit 0–9).
- Unlike traditional machine learning, **features are automatically extracted**.

### Advantages of Deep Learning
- Builds internal representation of features and combinations automatically.
- Manual specification of features may not be feasible.
- Supports **parallel computations**:
  - Data split into small batches.
  - Enables scalability and performance by handling large datasets efficiently.

### History of Deep Learning
- **1950s**: Concepts like artificial neuron, perceptron, and multi-layer perceptron.
- **1980s**: Introduction of **backpropagation** for training.
- **1990s**: Emergence of **convolutional neural networks (CNNs)** for image analysis.
- **2000s**: GPUs introduced.
- **2010s**: Cheaper, widely available GPUs fuel widespread adoption.
- **2012**: Major networks like **AlexNet** and **Deep-Q-Network** developed.
- **2016 onwards**: Generative deep learning use cases emerge.
- **Today**: Used in computer vision, NLP, speech recognition, text translation, large language models, and generative models.

### Applications of Deep Learning
- **Data types**:
  - Images
  - Videos
  - Text
  - Audio
- **Image applications**: classification, object detection, segmentation, facial recognition.
- **Text applications**: translation, sentiment detection.
- **Audio applications**: music generation, speech-to-text.
- **Selecting architecture**:
  - CNN → image tasks.
  - RNN, LSTM, Transformers → text tasks.
  - Transformers → text summarization, question answering.
  - GANs, Transformers, Diffusion Models → image generation.

### Artificial Neural Networks (ANNs)
- **Inspired by human brain** with interconnected neurons.
- **How neurons process inputs**:
  - Inputs have **weights**.
  - Weighted sum computed.
  - If sum exceeds threshold → neuron fires.
  - Outputs of one layer become inputs to next.

#### Building Blocks of ANN
1. **Layers**:
   - Input layer
   - Output layer
   - Hidden layers (optional)
2. **Neurons**: Computational units that accept inputs and produce outputs.
3. **Weights**: Strength of connections between neurons.
4. **Bias**: Additional input for flexibility.
5. **Activation functions**: Work on weighted sums to produce outputs.

### Example: Handwritten Digit Recognition
- Dataset: Images of **28×28 pixels**.
- **Input layer**: 28×28 pixels.
- **Output layer**: 10 neurons (digits 0–9).
- **Hidden layers**: Two layers with 16 neurons each.
- **Training**:
  - Show image to ANN.
  - Example: Input is digit "2".
  - If ANN predicts wrong (e.g., outputs "6"), error is detected.
  - **Backpropagation algorithm**:
    - Adjusts weights to reduce error.
    - Repeats with thousands of images.
    - ANN learns to predict correct digit.

## Important Terms
- **Deep Learning**: Subset of ML using ANNs to process raw data.
- **Artificial Neural Network (ANN)**: Brain-inspired network with neurons and layers.
- **Neuron**: Computational unit with inputs and outputs.
- **Weights**: Determine strength of connections between neurons.
- **Bias**: Extra input allowing flexibility.
- **Activation Function**: Determines output from weighted input sum.
- **Layers**: Input, hidden, output layers in an ANN.
- **Backpropagation**: Algorithm for adjusting weights during training.
- **CNN (Convolutional Neural Network)**: Architecture for image analysis.
- **RNN (Recurrent Neural Network)**, **LSTM (Long Short-Term Memory)**, **Transformers**: Architectures for text tasks.
- **GANs (Generative Adversarial Networks)** and **Diffusion Models**: Architectures for image generation.

## Summary
Deep learning is a subset of machine learning that leverages ANNs to automatically extract features from raw data, enabling tasks like image recognition, natural language processing, and speech-to-text. Its scalability is powered by parallel processing of data batches. The field has evolved from perceptrons in the 1950s to modern architectures such as CNNs, transformers, and generative models. ANNs consist of layers, neurons, weights, biases, and activation functions. Using training methods like backpropagation, ANNs can learn from large datasets, as illustrated by handwritten digit recognition.
