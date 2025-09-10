# AI Vector Search in Oracle Database 23ai - Learning Notes

## Overview
This lesson explains how **Oracle Database 23ai** has built-in **AI Vector Search** capabilities. It introduces the components of Vector Search, how it integrates with relational and unstructured data, and how it supports Gen AI pipelines with your data and applications. The video also covers SQL syntax, VECTOR datatype, VECTOR functions, Vector Indexes, similarity search, joins, and how these features enable Gen AI use cases directly in the database.

## Key Concepts
- **AI Vector Search**: Built into Oracle Database 23ai for semantic search across structured and unstructured data.
- **Converged Database**: Oracle supports JSON, XML, graph, spatial, text, relational, and vectors in one system.
- **VECTOR Datatype**: Stores vector embeddings in tables, even with relational data.
- **VECTOR_EMBEDDING Function**: Generates vectors from models for storage and search.
- **VECTOR_DISTANCE Function**: Calculates similarity between vectors using distance metrics (default cosine).
- **Vector Index**: Enhances performance and controls accuracy in similarity search queries.
- **Approximate Search**: Uses indexes for high-performance, target-accuracy similarity searches.
- **Similarity Search over Joins**: Enables searching across normalized enterprise data.
- **Gen AI Pipeline Integration**: Powers retrieval-augmented generation workflows with enterprise and unstructured data.
- **Third-Party Integration**: Supports LangChain and LamaIndex for advanced AI applications.

## Detailed Notes

### Built-in AI Vector Search
- Oracle Database 23ai integrates **AI Vector Search** natively.
- Supports **large language models**, **Gen AI capabilities**, and integration with **OCI Gen AI services**.
- Enables semantic information retrieval across structured and unstructured data.

### Database Features
- SQL support for **database-native vector generation**.
- **VECTOR datatype** to store embeddings.
- SQL syntax and functions for **similarity search**.
- **Approximate search index** tuned for high performance and quality.

### Model Integration
- Models can be accessed through **API calls** or loaded into the database as **ONNX models**.
- Example: **resnet_50** loaded into the database.
- Process:
  1. Pass model into **VECTOR_EMBEDDING** function with query image.
  2. Function returns a vector for storage and comparison.
  3. Perform similarity search to return top matches.

### VECTOR Datatype
- Added to allow vector columns in relational tables.
- Two formats:
  - With explicit dimension.
  - Simpler VECTOR specification without dimension format.
- Schema remains unchanged even as embedding models evolve.

### Similarity Search
- **VECTOR_DISTANCE** function calculates distances between vectors.
- Smaller distances = higher similarity.
- Distance metric can be changed (default: cosine).

### SQL Example
- AI Vector Search can combine data in **five lines of SQL**:
  - Matches candidate resumes with top 10 positions in preferred cities.
  - Combines applicant data, job data, and vector embeddings.
- Single integrated solution:
  - Fully consistent data.
  - Simple implementation.

### Vector Indexes
- Created like any other index.
- Improve **performance** and **accuracy control**.
- Options:
  - **Organization**:
    - `INMEMORY NEIGHBOR GRAPH` → for in-memory fit.
    - `NEIGHBOR PARTITIONS` → otherwise.
  - **Distance** clause (optional; default = COSINE).
  - **TARGET ACCURACY** clause:
    - Sets default or query-level accuracy for similarity searches.

### Approximate Search
- Use **APPROXIMATE** keyword in the FETCH clause.
- Example: Returning top 5 customers.
- If **target accuracy** = 80, results may include 4 out of 5 correct matches.
- If no Vector Index:
  - Exact search may be used.
  - SQL Optimizer may decide on index vs. exact search.

### Similarity Search over Joins
- Differentiator of Oracle Database 23ai.
- Supports joins because enterprise data is usually normalized.
- Example query joins three tables:
  - **Author**, **Books**, **Pages**.
  - Each **Page** has embeddings stored in a vector column.
- Query:
  - Searches embeddings in Pages with **qVec** text embedding.
  - Returns top 5 books containing text similar to query.
  - Adds conditions: book genre = fiction, author = from India.
- **Cost-based optimizer** decides join strategy and index usage.

### Gen AI Pipeline
- Data sources: database, CSV, social media, etc.
- Process:
  - Load documents.
  - Transform (summarize, split).
  - Generate vectors using embedding model.
  - Store in vector database.
- Enables:
  - Similarity searches.
  - RAG (Retrieval-Augmented Generation) pattern with LLMs.

### Integration
- Oracle Database 23ai fully supports Gen AI pipeline processing.
- Integrates with **LangChain** and **LamaIndex**.
- Provides **enterprise-grade performance and reliability**.
- Allows combining in a single query:
  - Relational, document, spatial, graph, ML, and Vector Search.
- Orchestration of Gen AI pipelines can be:
  - **Native in the database**.
  - **Through third-party frameworks**.

## Important Terms
- **AI Vector Search**: Semantic similarity search built into Oracle Database 23ai.
- **Converged Database**: Database supporting multiple data types (JSON, XML, graph, spatial, text, relational, vectors).
- **VECTOR Datatype**: Database type for storing vector embeddings.
- **VECTOR_EMBEDDING**: Function generating vectors from models.
- **VECTOR_DISTANCE**: Function computing similarity between vectors.
- **Vector Index**: Index to optimize similarity search performance and accuracy.
- **INMEMORY NEIGHBOR GRAPH**: In-memory vector index organization.
- **NEIGHBOR PARTITIONS**: Partitioned vector index organization.
- **TARGET ACCURACY**: Defines expected accuracy level in approximate searches.
- **APPROXIMATE**: Keyword for approximate similarity search using vector indexes.
- **qVec**: Example query vector used in join-based similarity search.
- **RAG (Retrieval-Augmented Generation)**: Design pattern for LLMs using retrieved vectors.

## Summary
Oracle Database 23ai integrates **AI Vector Search** as a core database feature. It provides:
- Native SQL support for vectors, embeddings, and similarity search.
- VECTOR datatype, VECTOR_EMBEDDING, and VECTOR_DISTANCE functions.
- Vector Indexes with options for organization, distance metrics, and target accuracy.
- Approximate and exact search flexibility.
- Ability to run similarity search queries over joins for normalized enterprise data.
- Integration with Gen AI pipelines, supporting diverse data sources and RAG patterns.
- Tight integration with LangChain and LamaIndex.
- Enterprise-grade performance for combining relational, unstructured, and AI-powered vector searches in a single query.
