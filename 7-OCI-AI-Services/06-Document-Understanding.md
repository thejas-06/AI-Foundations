# Document understanding - Learning Notes

## Overview
This lesson introduces the second major capability of **OCI Vision**, known as **Document AI**. It is designed for working with document images such as PDFs, JPEG, PNG, Tiff, or photographs containing textual information. The focus is on extracting, classifying, and analyzing text and data within documents.

## Key Concepts
- **Document AI**: A capability of Vision for understanding document images, including PDFs and common image formats.
- **Text Recognition (OCR)**: Extracts text from images, even in challenging cases like handwritten text, tilted, shaded, or rotated documents.
- **Document Classification**: Classifies documents into 10 different types using visual appearance, high-level features, and extracted keywords.
- **Language Detection**: Determines the language of the text by analyzing visual features rather than relying on the text itself.
- **Table Extraction**: Identifies tables in documents and extracts their content in a tabular format.
- **Key Value Extraction**: Finds values for 13 common fields and line items in receipts, such as merchant name and transaction date.

## Detailed Notes
- **Supported Document Types**:
  - PDFs
  - Document image types (JPEG, PNG, Tiff)
  - Photographs containing textual information

- **Features of Document AI**:
  - **Text Recognition (OCR)**:
    - Extracts text from images.
    - Handles difficult scenarios such as handwritten texts.
    - Works with tilted, shaded, or rotated documents.
  - **Document Classification**:
    - Classifies documents into 10 types.
    - Uses visual appearance, high-level features, and extracted keywords.
    - Example use cases: invoices, receipts, resumes.
  - **Language Detection**:
    - Determines the language based on visual text features.
    - Does not rely solely on the text itself.
  - **Table Extraction**:
    - Detects tables within documents.
    - Extracts content into tabular form.
  - **Key Value Extraction**:
    - Identifies values for 13 predefined fields and line items in receipts.
    - Examples: merchant name, transaction date.

## Summary
OCI Vision’s **Document AI** capability processes document images such as PDFs and common image formats. It provides features including text recognition (OCR), classification into document types, language detection, table extraction, and key value extraction. These tools make it possible to automate the understanding and processing of complex document images efficiently.
