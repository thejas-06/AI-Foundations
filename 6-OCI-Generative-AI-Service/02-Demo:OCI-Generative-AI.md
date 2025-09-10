# OCI Generative AI Service Demo - Learning Notes

## Overview
This demo walks through the **OCI Generative AI Service** in the OCI Console. It covers availability of the service by region, navigating the console, using the **playground** to explore pretrained chat and embedding models, generating and modifying outputs, obtaining code for integration, and managing advanced features like **dedicated AI clusters**, **custom models**, and **endpoints**.

## Key Concepts
- **Generative AI Service**: OCI’s hosted service for exploring pretrained and custom generative AI models.
- **Playground**: A visual interface for experimenting with models without writing code.
- **Chat Models**: Pretrained models that retain conversational context (e.g., Command-R, Command-R-Plus, Llama 3).
- **Embedding Models**: Convert text into vectors for semantic search and clustering.
- **Dedicated AI Clusters**: GPU-based resources for fine-tuning and hosting models.
- **Custom Models**: Fine-tuned versions of pretrained models.
- **Endpoints**: Hosted interfaces for serving inference traffic.

## Detailed Notes
### Accessing the Service
- Logged into OCI Console in **Germany Central (Frankfurt)** region.
- Generative AI Service is only available in select regions.
- Navigation:
  - Use **burger menu** → **Analytics and AI** → **AI Services** → **Generative AI**.

### Dashboard
- Options include:
  - **Service tool** (video resources).
  - **Documentation** (service and API details).
  - **Playground** for model experimentation.
- Dashboard also shows:
  - **Dedicated AI Clusters** (GPU-based compute).
  - **Custom Models** (fine-tuned models).
  - **Endpoints** (hosted inference points).

### Playground
- Visual interface for exploring models without code.
- Supports **Chat Models** and **Embedding Models**.

#### Chat Models
- Available models:
  - **Command-R** (affordable, up to 16,000 tokens).
  - **Command-R-Plus** (more powerful, up to 128,000 tokens).
  - **Meta Llama 3 (70B instruct)** (8,000 token limit).
- Key details:
  - Models keep conversation context.
  - Example prompt: *“Teach me how to fish.”*
  - Follow-up prompt: *“Describe step 3.”* → remembers context and expands.
- Code integration:
  - **View Code** → choose Java or Python.
  - Example shows inference client, API call, variables setup.
  - Code can be copied into IDEs like Jupyter Notebook.
- Adjusting outputs:
  - **Preamble override**: Change style/tone (e.g., “travel advisor with pirate code”).
  - **Temperature**: Controls randomness of outputs.

#### Embedding Models
- Convert text to numeric vectors for **semantic search**.
- Demonstration with **41 HR Help Center articles**:
  - Converts titles into embeddings.
  - Visualized in 2D clusters (though actual vectors have hundreds of dimensions).
  - Articles with similar meaning group together.
    - Example: Article 24 = technical skills, Article 19 = career development.
    - Other clusters: leave, vacation, time card.
- Semantic similarity:
  - Numerically close vectors = semantically similar text.
  - Enables search by meaning rather than keywords.
- Code also available for embedding integration into AI applications.

### Advanced Features
#### Dedicated AI Clusters
- GPU-based compute resources.
- Created by:
  - **Create Dedicated AI Cluster** → provide name → choose purpose (hosting or fine-tuning).
  - Select pretrained models and create.
- Supports both inference and fine-tuning workloads.

#### Custom Models
- Created by fine-tuning pretrained models.
- Steps:
  1. **Create Model** → provide name → click Next.
  2. Choose **base model**.
  3. Select **fine-tune method**.
  4. If no cluster exists, create a **Dedicated AI Cluster** here.
- Fine-tuning requires GPU-based clusters.

#### Endpoints
- Serve inference traffic for fine-tuned models.
- Steps:
  1. **Create Endpoint**.
  2. Provide name, hosting configuration, and hosted model.
  3. Requires a **Dedicated AI Cluster**.
- Once created, endpoints allow fine-tuned models to serve production traffic.

## Important Terms
- **Generative AI Service**: OCI platform for pretrained and fine-tuned models.
- **Playground**: No-code interface for experimenting with models.
- **Chat Models**: Models that retain conversational context.
- **Embedding Models**: Numeric vector representations of text for semantic search.
- **Preamble Override**: Custom instruction to alter chat model behavior.
- **Temperature**: Parameter controlling randomness of model output.
- **Dedicated AI Cluster**: GPU-based compute for hosting or fine-tuning.
- **Custom Model**: Fine-tuned model built on top of a pretrained model.
- **Endpoint**: Interface to serve inference traffic from hosted models.

## Summary
The OCI Generative AI Service provides:
- A **dashboard** with access to playground, clusters, models, and endpoints.
- A **playground** for experimenting with **chat** and **embedding models**.
- Tools for refining model outputs using **preamble overrides** and **temperature**.
- Integration options by copying **auto-generated code** in Python/Java.
- Support for **dedicated AI clusters**, **fine-tuned custom models**, and **endpoints** to deploy production-ready AI applications.
