# Large Language Models (LLMs) - Learning Notes

## Overview
In this lesson, we explore **large language models (LLMs)**.  
The video explains what a language model is, how it predicts words, how probabilities are assigned, the meaning of "large" in LLMs, examples of applications, their underlying architecture, and the scale of their parameters.

---

## Key Concepts

- **Language Model**: A probabilistic model of text that determines the likelihood of a word appearing based on the previous words.
- **Vocabulary**: The set of words that the model considers possible in a given context.
- **Probability Distribution**: Each word in the vocabulary is assigned a probability of appearing in the next position.
- **Large Language Model (LLM)**: Refers to language models with a very high number of parameters.
- **Parameter**: Adjustable weights in the neural network optimized during training.
- **Transformer Architecture**: The deep learning architecture that powers LLMs, allowing them to focus on different parts of the input for better predictions.
- **End of Sentence (EOS)**: A special token that indicates the completion of a sequence.

---

## Detailed Notes

### What is a Language Model?
- A language model is a probabilistic model of text.  
- It determines the probability of a given sequence of words based on the previous words.  
- Example:  
  *Sentence*:  
  > "I wrote to the zoo to send me a pet. They sent me ___."

#### Probability Distribution Example

| Word      | Probability |
|-----------|-------------|
| Lion      | 0.03        |
| Elephant  | 0.02        |
| Dog       | 0.45        |
| Cat       | ...         |
| Panther   | ...         |

- Words outside the vocabulary (e.g., *car, truck, building*) are **not considered**, since they are not relevant to the context.

---

### Large Language Models
- The **"large"** in large language models refers to the **number of parameters**.  
- No fixed threshold defines what is large or small.  
- Collectively, these models are called large language models.

---

### How Word Selection Works
- The model picks the word with the **highest probability**.  
- In the earlier example, **"dog"** had the highest probability.  
- After appending "dog" and re-feeding it, probabilities of other words change.  
- Example:  
  - Elephant → 0.02 → **0.001**  
  - Dog drops further  
- A new token **EOS (end of sentence)** appears with very high probability.  
- The model suggests ending the sentence:  
  > "I wrote to the zoo to send me a pet. They sent me a dog."  

---

### Applications of Large Language Models
- **Answering questions**  
  - Example: "What is the capital of France?" → *Paris*  
- **Reasoning over puzzles** with explanations  
- **Writing articles/essays**  
  - Example: Essay on the French Revolution  
- **Translation**  
  - Example: Translate *"How are you"* into French → *Comment allez-vous* (formal French)  

---

### Architecture
- LLMs use the **transformer architecture**.  
- Transformers allow models to pay **selective attention** to different parts of input.  
- This provides enhanced **contextual understanding**.

---

### Capabilities
- LLMs perform well in **natural language understanding** tasks such as:  
  - Question answering  
  - Language translation  
  - Sentiment analysis  
  - Summarization  

---

### Training and Parameters
- LLMs are **deep neural networks** trained on massive amounts of internet text.  
- **Parameters**: Adjustable weights optimized to predict the next word in a sequence.  
- **Model size**: The memory required to store parameters and supporting structures.  
- Growth trend: Parameter counts have grown exponentially, with some models reaching **540 billion parameters**.  
- Some models do not disclose their parameter count (could be higher).  
- **Key Point**: Bigger models are not always better → risk of **overfitting**.

---

## Important Terms

- **Language Model**: Probabilistic model predicting words in a sequence.  
- **Vocabulary**: The set of words considered by the model.  
- **Probability Distribution**: Probabilities assigned to vocabulary words.  
- **Large Language Model (LLM)**: Language model with a large number of parameters.  
- **Parameter**: Adjustable weights optimized during training.  
- **Transformer**: Neural architecture enabling selective attention and contextual understanding.  
- **EOS (End of Sentence/Sequence)**: Token marking the end of output.  
- **Overfitting**: Model memorizing training data too closely, harming generalization.  

---

## Summary
- **LLMs** are probabilistic models predicting the next word in a sequence.  
- They assign probabilities to words in a **vocabulary** and select the most likely one.  
- The **large** in LLMs refers to **number of parameters** (millions → billions).  
- Based on the **transformer architecture**, LLMs provide contextual predictions.  
- Applications: **Q&A, reasoning, writing, translation, summarization, sentiment analysis**.  
- Larger models don’t always perform better → risk of **overfitting**.  
