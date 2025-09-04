# Transformer Architecture (Part 1) - Learning Notes

## Overview
This lesson introduces the **transformer architecture** and contrasts it with **recurrent neural networks (RNNs)**.  
It explains why understanding language can be tricky for machines, the limitations of RNNs in handling long sequences, and how **transformers** with the **self-attention mechanism** overcome these challenges.  
It also introduces the **encoder-decoder structure** of transformers and sets the stage for the next lesson.

---

## Key Concepts
- **Recurrent Neural Networks (RNNs)**: Neural networks designed for sequential data, using hidden states to maintain context.
- **Hidden State / Memory**: Internal state that persists across time steps, updated as each element in a sequence is processed.
- **Vanishing Gradient**: The difficulty RNNs face in capturing long-range dependencies as sequences grow longer.
- **Transformer Architecture**: A deep learning model introduced in *Attention Is All You Need*, which processes all words in a sequence simultaneously.
- **Self-Attention Mechanism**: Adds context to text by weighing the importance of different words relative to each other, enabling transformers to capture long-range dependencies.
- **Encoder-Decoder Structure**: Submodules of transformers where the encoder processes input text into vectors, and the decoder generates output text.

---

## Detailed Notes  

### Example Sentence
- Sentence:  
  > "Jane threw the Frisbee and her dog fetched it."  
- Humans understand easily:
  - *Jane* is doing the throwing  
  - *Dog* is doing the fetching  
  - *Frisbee* is the object being thrown  
  - *It* refers to the frisbee  
- For machines, understanding "it" correctly is tricky.

---

### Recurrent Neural Networks (RNNs)
- RNNs are designed to handle sequential data like sentences.
- They process **input data one element at a time**, maintaining a **hidden state** across time steps.
- Steps in processing the example sentence:
  - Step 1 → Model knows about *Jane*  
  - Step 2 → Model knows about *Jane* and *threw*  
  - Step 3 → Model knows about *Jane, threw, and*  
  - And so on...
- **Limitations**:
  - Capture only nearby dependencies.  
  - Struggle with long-range dependencies.  
  - As sequence length increases, relevant context is lost.  
  - Leads to the **vanishing gradient** problem.

---

### Transformer Architecture
- Transformers understand relationships between **all words in a sentence simultaneously**.
- Instead of sequential processing, they take a **bird’s-eye view** of the entire sentence.
- Example:
  - Connection between *Jane* and *dog* is understood, even though they are far apart.
- Unlike RNNs, transformers analyze the whole context at once.

---

### Self-Attention Mechanism
- Core feature of transformers.  
- Adds **context** by weighing the importance of words relative to each other.  
- Example sentence revisited:
  - *Dog* comes after *frisbee*  
  - *Fetched* comes after *dog*  
  - *It* comes after *fetched*  
  - Model determines that *it* likely refers to *frisbee*.
- Benefits:
  - Captures **long-range dependencies**.  
  - Enhances understanding of **contextual relationships** in text.

---

### Encoder-Decoder Architecture
- Transformers consist of two submodules:  
  - **Encoder**: Processes input text into **vectors** (numerical representations capturing context).  
  - **Decoder**: Takes encoded vectors and **generates output text**.  
- Both encoder and decoder use multiple layers connected by self-attention.  
- Note: Details of encoder-decoder will be covered in **Part 2** of this series.

---

## Important Terms
- **RNN (Recurrent Neural Network)**: Sequential model using hidden states for context.  
- **Hidden State / Memory**: Internal state updated at each time step to preserve sequence information.  
- **Vanishing Gradient**: Loss of ability to capture long-range dependencies in RNNs.  
- **Transformer**: Deep learning model that processes all input words simultaneously.  
- **Self-Attention**: Mechanism allowing models to weigh importance of words in relation to each other.  
- **Encoder**: Module that encodes input into contextual vectors.  
- **Decoder**: Module that generates output from encoded vectors.  
- **Vectors**: Numerical representations capturing context of input.  
- **Attention Is All You Need**: Paper that introduced the transformer architecture.

---

## Summary
- Understanding language is easy for humans but tricky for machines.  
- **RNNs** handle sequential data but fail with long-range dependencies due to the **vanishing gradient problem**.  
- **Transformers** overcome this by analyzing all words in parallel, enabling a holistic understanding of sentences.  
- **Self-attention** allows transformers to weigh contextual importance and resolve references like *“it” → frisbee*.  
- Transformers are built on an **encoder-decoder architecture** powered by self-attention.  
- In **Part 2**, encoder-decoder details will be explored further.
