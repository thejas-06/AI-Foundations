# OCI Language - Learning Notes

## Overview
OCI Language analyzes unstructured text using models trained on industry data. It enables language analysis without requiring data science experience. The service offers five main capabilities.

## Key Concepts
- **Language Detection**: Identifies the language of the input text, supporting 75 languages.
- **Entity Recognition**: Detects specific entities such as names, places, dates, emails, currency, organizations, and phone numbers (14 types total).
- **Sentiment Analysis**: Determines the sentiment of the text, both overall and at the aspect level, as well as sentence by sentence.
- **Key Phrase Extraction**: Identifies important ideas or subjects in the text.
- **Text Classification**: Categorizes the text into one of 600 categories and subcategories.

## Detailed Notes
- OCI Language analyzes unstructured text for the user.  
- It uses **models trained on industry data**, eliminating the need for data science expertise.  
- The service provides **five main capabilities**:  

  1. **Language Detection**  
     - Recognizes the language of the text.  
     - Supports 75 languages, from Afrikaans to Welsh.  

  2. **Entity Recognition**  
     - Identifies entities such as:  
       - Names  
       - Places  
       - Dates  
       - Emails  
       - Currency  
       - Organizations  
       - Phone numbers  
     - Supports 14 entity types in total.  

  3. **Sentiment Analysis**  
     - Identifies the sentiment expressed in the text.  
     - Provides sentiment not only for the entire block of text, but also for **different aspects**.  
     - Example:  
       - A restaurant review says: *“The food was great, but the service sucked.”*  
       - OCI Language recognizes:  
         - **Food** → Positive sentiment  
         - **Service** → Negative sentiment  
     - Also analyzes sentiment for **each sentence**.  

  4. **Key Phrase Extraction**  
     - Finds key phrases that represent important ideas or subjects in the text.  

  5. **Text Classification**  
     - Assigns a general topic to the text.  
     - Uses a predefined list of **600 categories and subcategories**.  

## Important Terms
- **Unstructured text**: Text without predefined data models or structure.  
- **Language Detection**: Identifying which language a text is written in.  
- **Entities**: Specific types of information (e.g., names, places, dates, emails, currency, organizations, phone numbers).  
- **Sentiment**: The expressed opinion or feeling (positive, negative, neutral) in text.  
- **Aspects**: Specific parts of a text that can have different sentiments (e.g., food vs. service in a review).  
- **Key Phrases**: Words or short phrases that represent the main ideas of the text.  
- **Categories**: Predefined topics used to classify text (600 available in OCI Language).  

## Summary
OCI Language provides a powerful way to analyze unstructured text without needing data science knowledge. It can:  
- Detect 75 languages  
- Recognize 14 types of entities  
- Analyze overall and aspect-based sentiment, including sentence-level analysis  
- Extract key phrases  
- Classify text into 600 categories and subcategories  
