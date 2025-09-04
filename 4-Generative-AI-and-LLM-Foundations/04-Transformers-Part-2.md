# Transformer Architecture (Lesson 2) - Learning Notes

## Overview
This lesson explains the **transformer architecture** with a focus on its two main components: the **encoder** and the **decoder**. It introduces essential concepts like **tokens**, **tokenization**, and **embeddings**, followed by detailed discussions on **encoder-only models**, **decoder-only models**, and **encoder-decoder models**. It also covers applications such as **semantic search**, **vector databases**, and **sequence-to-sequence tasks** like translation.

---

## Key Concepts
- **Encoder**: Reads input text, converts it into embeddings capturing meaning.
- **Decoder**: Uses embeddings to generate output text, producing tokens one at a time.
- **Tokens and Tokenization**: Input text is broken into smaller units called tokens, which may be entire words, parts of words, or punctuation symbols.
- **Embeddings**: Numerical or vector representations of text, enabling computers to understand relationships between pieces of text.
- **Semantic Search**: Technique to retrieve documents based on meaning using embeddings and vector databases.
- **RAG (Retrieval-Augmented Generation)**: Architecture where embeddings and retrieval enhance responses from large language models.
- **Transformer Variants**:
  - Encoder-only models: Focus on understanding input.
  - Decoder-only models: Generate sequences one token at a time.
  - Encoder-decoder models: Combine both for tasks like translation.

---

## Detailed Notes

### Encoder and Decoder
- Transformer models consist of two parts:
  - **Encoder**: Reads input text and encodes it into embeddings that capture meaning.
  - **Decoder**: Uses embeddings to generate the output text.

### Tokens and Tokenization
- Models process **tokens** instead of words.
- **Token** examples:
  - A token can be a whole word: *apple*.
  - A token can be part of a word: *friendship* → *friend* + *ship*.
  - Tokens can also be punctuation symbols: `,`, `.`, `:`.
- Number of tokens per word depends on text complexity:
  - Simple words: ~1 token per word.
  - Complex text: 2–3 tokens per word.
- Example: A sentence can map to 15 tokens, with common words like *many* and *words* as single tokens, rare words split into multiple tokens, and punctuation as separate tokens.

### Embeddings
- **Embeddings** are numerical representations of text.
- Text units can be: word, phrase, sentence, paragraph, or multiple paragraphs.
- Purpose: To help computers understand relationships between text.
- Example process:
  - Words like *they sent me a* → tokenized.
  - Tokens fed to an **encoder model**.
  - Output: numerical vector representations.
  - Outputs include vectors for each token and one for the whole sentence.
- Embeddings are used for:
  - Classification tasks.
  - **Vector databases**.
  - **Semantic search**: Input query is encoded, compared with encoded documents, and most relevant documents retrieved.
- Used in **RAG**: Encoded content + LLM knowledge = informed answers.

### Decoder Models
- Take a sequence of tokens and output the **next token**.
- Example:
  - Input: *They sent me a*.
  - Output: next token, e.g., *lion*.
- Characteristics:
  - Output one token at a time.
  - Can be invoked repeatedly to generate longer sequences.

### Encoder-Decoder Models
- Combine encoder and decoder.
- Common use: **sequence-to-sequence tasks** like translation.
- Process:
  - Input text tokenized → passed to encoder → embeddings generated.
  - Embeddings passed to decoder.
  - Decoder outputs tokens one at a time, with **self-referential loops**:
    - Each generated token is fed back into the decoder with the sequence to generate the next token.

### Transformer Variants Recap
- **Encoder-only models**:
  - Transform input into embeddings.
  - Applications: RAG, semantic search, vector databases.
- **Decoder-only models**:
  - Generate sequences based on given input.
  - Applications: text generation (articles, writing tasks).
- **Encoder-decoder models**:
  - Input via encoder, generation via decoder.
  - Applications: translation and other sequence-to-sequence tasks.

---

## Important Terms
- **Encoder**: Model component that converts input text into embeddings.
- **Decoder**: Model component that generates tokens one at a time from embeddings.
- **Token**: A word, part of a word, or punctuation symbol.
- **Tokenization**: Process of splitting text into tokens.
- **Embedding**: Numerical/vector representation of text.
- **Vector Representations**: Another name for embeddings.
- **Vector Database**: Storage for embeddings used in semantic search and retrieval tasks.
- **Semantic Search**: Retrieving documents by meaning, not exact word match.
- **RAG (Retrieval-Augmented Generation)**: Framework where retrieval enhances model outputs.
- **Self-Referential Loops**: Decoder feedback mechanism generating sequences token by token.

---

## Summary
- Transformer architecture has two main parts: **encoder** and **decoder**.  
- Encoders create embeddings; decoders generate tokens sequentially.  
- **Tokens** are the building blocks of model input, produced via **tokenization**.  
- **Embeddings** represent text numerically, enabling classification, semantic search, and RAG.  
- **Decoder-only models** generate text sequences one token at a time.  
- **Encoder-decoder models** are used for sequence-to-sequence tasks such as translation, with self-referential loops in the decoding process.  
- Variants of transformer architecture are designed for different tasks: encoder-only for understanding input, decoder-only for generating data, and encoder-decoder for translation-like tasks.
