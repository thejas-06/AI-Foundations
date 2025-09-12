# OCI Language in the Console - Learning Notes

## Overview
This video walks through using **OCI Language** in the Oracle Cloud Console. It covers how to navigate to the service, available resources, and demonstrates text analysis features including **language detection**, **classification**, **named entity recognition**, **key phrase extraction**, and **sentiment analysis**.

## Key Concepts
- **OCI Language Service**: An AI service under Analytics & AI in the Oracle Cloud Console.
- **Resources**: Links to documentation, API reference, SDK guide, and blogs related to the service.
- **Text Analytics**: A feature to analyze input text with multiple types of language processing.
- **Language Detection**: Identifies the language of the text with confidence scores.
- **Classification**: Assigns categories and subcategories to text.
- **Named Entities**: Highlights entities, their types, and confidence levels.
- **Key Phrase Extraction**: Lists important key phrases from the text.
- **Sentiment Analysis**: Provides document-level, aspect-based, and sentence-level sentiment results.

## Detailed Notes
- Start from the **OCI Console home screen** (appearance may vary).
- Navigate: **Menu → Analytics & AI → AI Services → Language**.
- **Language page**:
  - Provides links to documentation on specific topics.
  - Includes resources like the API reference, SDK guide, and blogs.
- **Trying the Service**:
  - Select **Text Analytics**.
  - Default text is provided for testing.
  - Click the **Analyze** button to process the text.
- **Analysis Results**:
  1. **Language Detection**:
     - Example detected: English.
     - Confidence: Very high.
  2. **Classification**:
     - Category: Science and technology.
     - Subcategory: Earth sciences.
     - Probability: Fairly low.
     - Still accurate in this example.
  3. **Named Entities**:
     - Entities highlighted in the text.
     - Shows: entity name, type, and confidence.
     - Different color coding for types:
       - Locations
       - Quantities
       - Products
       - Date times
  4. **Key Phrase Extraction**:
     - Lists all key phrases extracted from the text.
  5. **Sentiment Analysis**:
     - **Document-level sentiment**:
       - Refers to the whole text.
       - Example: Mixed.
     - **Aspect-based sentiment**:
       - Identifies specific aspects in the text.
       - Assigns sentiments to those aspects.
       - In this case: all negative.
     - **Sentence-level sentiment**:
       - Each sentence assigned: positive, neutral, or negative.
       - Example contained a mix of all three.

## Important Terms
- **OCI Language Service**: AI service for analyzing text within Oracle Cloud.
- **Text Analytics**: Tool for running analysis on input text.
- **Language Detection**: Identifies the text’s language with confidence scores.
- **Classification**: Assigns text to categories and subcategories with probabilities.
- **Named Entities**: Specific elements in the text, labeled with type and confidence.
- **Key Phrase Extraction**: Pulls out key phrases from the text.
- **Sentiment Analysis**: Determines sentiment at document, aspect, and sentence levels.

## Summary
The OCI Language service in the Oracle Cloud Console enables users to analyze text through features like **language detection**, **classification**, **named entity recognition**, **key phrase extraction**, and **sentiment analysis**. The console provides built-in resources and an interactive interface to explore these capabilities, giving a clear view of what the service can produce in terms of text analysis.
