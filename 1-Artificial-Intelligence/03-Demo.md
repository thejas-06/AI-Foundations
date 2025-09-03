# OCI AI Services - Learning Notes  

## Overview  
This lesson introduces **Oracle Cloud Infrastructure (OCI) AI services** with hands-on demonstrations.  
It focuses on two services:  
1. **Vision AI Service** – for analyzing images and documents.  
2. **Language AI Service** – for analyzing and translating text.  

---

## Key Concepts  
- **Vision AI Service**: Performs image classification, object detection, text detection, and document AI.  
- **Confidence Scores**: Each detected label or object includes a confidence percentage.  
- **Document AI (Document Understanding)**: Extracts text, key-value pairs, and tables from documents.  
- **Language AI Service**: Provides text analysis (language detection, classification, sentiment, entities, key phrases, PII detection) and text translation.  
- **Custom Models**: Users can train AI services with their own data.  

---

## Detailed Notes  

### 1. Vision AI Service  
Supports multiple tasks:  

#### a) Image Classification  
- Detects labels within an image and assigns **confidence scores**.  
- Example:  
  - Vegetation detected with **99.23% confidence**.  
  - Zebra image detected with labels like *zebra, vegetation, grassland, plant, animal, mammal, sky*.  

#### b) Object Detection  
- Provides **bounding boxes** around detected objects with labels and confidence scores.  
- Examples:  
  - Traffic image → detected multiple cars, taxis, and people.  
  - Basket of fruit → detected *orange, banana, apple, bowl*.  

#### c) Text Detection  
- Extracts text written on objects or surfaces in images.  
- Examples:  
  - Bus image → detected text on the bus, including license plate **M32HOD** and number **45**.  
  - Image with multiple fonts → scanned line by line (e.g., *Arial, Arial Black*).  

#### d) Document AI (Document Understanding)  
- Previously part of Vision AI but now a separate service.  
- Features remain the same.  
- Example (Receipt analysis):  
  - Extracted **raw text** line by line.  
  - Identified **key-value pairs**: transaction date, transaction time, subtotal, tax, total.  
  - Extracted **tables**:  
    1. Main items table  
    2. Total summary table  
    3. Authorization details table (e.g., terminal ID, amount, card authorization code).  

---

### 2. Language AI Service  

#### a) Text Analysis  
Applies pretrained models to analyze a block of text. Capabilities include:  
- **Language Detection** → identified input text as *English*.  
- **Text Classification** → classified as *science and technology / computer-related*.  
- **Entity Extraction** → detected entities like *food, computers, manual instruments*, tagged as *product* or *event*.  
- **Key Phrase Extraction** → phrases like *early computers*, *simple manual instruments*.  
- **Sentiment Analysis** →  
  - **Aspect-based sentiments** (subject-level, e.g., food, early computers)  
  - **Sentence-level sentiments** (negative or neutral)  
- **Personal Identifiable Information (PII) Detection** → detected sensitive items (e.g., *World War II*, related dates).  

#### b) Text Translation  
- Supports multiple source and target languages.  
- Example:  
  - Translated English text into **French**.  
  - Translated English text into **Japanese**.  

#### c) Custom Models  
- Users can train models with their own data for domain-specific tasks.  

---

## Important Terms  
- **Image Classification**: Assigning category labels to an image.  
- **Object Detection**: Identifying objects in an image with bounding boxes.  
- **Text Detection**: Extracting written content from an image.  
- **Document AI / Document Understanding**: Extracting structured information (text, key-value pairs, tables) from documents.  
- **Confidence Score**: Probability assigned by the model indicating certainty of detection.  
- **Entities**: Identified items within text (e.g., products, events).  
- **Aspect-based Sentiment**: Sentiment associated with a particular subject or entity.  
- **Sentence-level Sentiment**: Overall polarity (positive, negative, neutral) of a sentence.  
- **PII (Personal Identifiable Information)**: Sensitive data like names, dates, numbers, or identifiers.  

---

## Summary  
The **OCI Vision AI Service** provides capabilities like image classification, object detection, text detection, and document analysis, with results including confidence scores, labels, and structured extraction.  
The **OCI Language AI Service** offers text analysis (language detection, classification, entities, key phrases, sentiment, PII) and text translation across multiple languages. Users can also train **custom models**.  

Together, these services allow developers to automate image, document, and text analysis tasks effectively on OCI.  
