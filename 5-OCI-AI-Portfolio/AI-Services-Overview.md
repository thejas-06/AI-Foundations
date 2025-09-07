# OCI AI Services - Learning Notes

## Overview
In this lesson, the focus is on **OCI AI services**. Oracle has been investing across the enterprise stack, beginning with data and infrastructure layers, and extending to SaaS applications. OCI AI services consume data, and applications in turn consume these services. Oracle AI provides a portfolio of cloud services that help organizations use their data for business-specific purposes.  

This session covers how OCI AI services work, their methods of access, and the different AI services offered such as Digital Assistant, Language, Vision, Speech, and Document Understanding.

---

## Key Concepts
- **Oracle AI Portfolio**: Cloud services designed to help organizations use their data for business purposes.
- **AI Services Consumption**: Applications consume AI/ML services, which rely on data as the foundation.
- **Prebuilt and Custom Models**: Services include pretrained models for general use, and the ability to train custom models with customer data.
- **Access Methods**: Console, REST API, SDKs, and CLI are available for interacting with OCI AI services.
- **OCI AI Services Collection**: Includes prebuilt ML models for business applications, customizable for more accurate results.
- **Types of Services**:
  - Digital Assistant
  - Language
  - Vision
  - Speech
  - Document Understanding

---

## Detailed Notes

### Oracle AI and Enterprise Stack
- Oracle invests across layers: **data → infrastructure → applications**.
- AI services consume data and provide results to applications.
- Recent advancements: **Generative AI** and **massive scale models**.

### Foundation of AI Services
- **Data** is the foundation of AI and ML services.
- **AI services** provide prebuilt models for specific business uses.
- Models can be:
  - **Pretrained** for general use.
  - **Custom trained** with customer data for domain-specific results.
- AI services are accessed by calling the **API** with input data, and receiving results.
- No infrastructure management is required for use.

### Access Methods
- **OCI Console**: Browser-based interface for notebook sessions and features of data science and AI services.
- **REST API**: Requires programming expertise, provides service functionality with API reference.
- **Language SDKs**: Available for Java, Python, TypeScript/JavaScript, .NET, Go, and Ruby.
- **Command Line Interface (CLI)**: Offers both quick access and full functionality without scripting.

### Collection of OCI AI Services
Prebuilt machine learning models to simplify application development, with custom training options for accuracy.

#### 1. **Language Service**
- **Text Analysis at Scale** using pretrained and custom models.
- **Capabilities**:
  - **Pretrained Models**:
    - Language detection
    - Sentiment analysis
    - Key phrase extraction
    - Text classification
    - Named entity recognition (NER)
    - Personally identifiable information (PII) detection
  - **Custom Models**:
    - NER with domain-specific datasets
    - Text classification
  - **Text Translation**:
    - Neural machine translation across many languages.

#### 2. **Vision Service**
- **Image Analysis**:
  - **Pretrained Models**:
    - Object detection
    - Image classification
    - Optical character recognition (OCR)
  - **Custom Models**:
    - Custom object detection (bounding box for custom objects)
    - Custom image classification (identify objects and scene-based features)

#### 3. **Speech Service**
- Converts **media files** containing human speech into text.
- Output formats: **JSON** and **SRT**.
- Enables accurate transcriptions.

#### 4. **Document Understanding Service**
- Upload documents for **text and object detection/classification**.
- Process individual or batch files.
- **Capabilities**:
  - OCR: Detect and recognize text in documents.
  - Text Extraction: Provides word-level and line-level text, plus bounding box coordinates.
  - Key Value Extraction: Extracts info from receipts, invoices, passports, driver IDs.
  - Table Extraction: Extracts tabular content, preserving rows and columns.
  - Document Classification: Classifies documents into types.

#### 5. **Oracle Digital Assistant**
- Platform for creating and deploying **AI-driven interfaces** using natural language conversations.
- **Capabilities**:
  - Greets users and lists available functions.
  - Routes user input to appropriate **skills**.
  - Provides entry points into skills.
  - Handles explicit requests, interruptions, disambiguation, and exit requests.

---

## Important Terms
- **OCI AI Services**: Oracle Cloud Infrastructure services with prebuilt machine learning models.
- **Pretrained Models**: Ready-to-use models for general tasks like sentiment analysis or object detection.
- **Custom Models**: Models trained with customer-specific data for tailored results.
- **OCI Console**: Browser-based interface for accessing AI services.
- **REST API**: Application programming interface for service access requiring coding.
- **Language SDK**: Software development kits for programming languages (Java, Python, etc.).
- **CLI (Command Line Interface)**: Text-based tool for accessing AI service functionality.
- **OCR (Optical Character Recognition)**: Detecting and recognizing text in images or documents.
- **NER (Named Entity Recognition)**: Identifying entities like names, organizations, locations from text.
- **Digital Assistant**: AI-driven conversational interface.

---

## Summary
OCI AI services provide enterprises with a portfolio of cloud-based AI tools built on Oracle’s data and infrastructure stack. These services offer pretrained and customizable models for business applications without infrastructure management. Access is available via console, REST API, SDKs, and CLI.  

The key services include:
- **Language**: Text analysis, translation, and custom modeling.
- **Vision**: Object detection, classification, OCR, and custom image analysis.
- **Speech**: Conversion of spoken media into accurate text.
- **Document Understanding**: Extraction and classification of structured and unstructured document content.
- **Digital Assistant**: Conversational AI for natural language interaction.

Together, these services simplify AI adoption for enterprises by enabling efficient and scalable integration of AI into applications.
