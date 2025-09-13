# Demo of Document understanding - Learning Notes

## Overview
This video segment demonstrates the use of **Document AI** to process document images, specifically receipts and invoices. It highlights capabilities such as text extraction, key value recognition, line item data, and tabular data processing.

## Key Concepts
- **Text Extraction**: Extracts raw text from receipts and invoices, both in line format and individual word format.
- **Key Value Extraction**: For receipts, specific keys such as merchant name, address, phone number, transaction time, and transaction date are identified and matched with values.
- **Line Item and Tabular Data**: Extracts structured information such as purchased items, quantities, descriptions, unit price, and totals.
- **Handling Handwritten and Stamped Text**: Document AI can extract information even from handwritten or stamped content, though readability may vary.

## Detailed Notes
- The default image example is a **receipt**:
  - Detected as English.
  - Extracted all raw text from the receipt, shown as both line format and individual word format.
  - Key values identified:
    - Merchant name: *example cafe*
    - Merchant address
    - Merchant phone number
    - Transaction time
    - Transaction date
  - Line item data was extracted, including:
    - *Americano*
    - *Water*
  - Tabular data representing the items was also recognized.

- A second example is an **invoice**:
  - All text on the image was extracted and highlighted.
  - The invoice included a **stamp** applied by an accounts payable clerk after processing.
    - Some of the stamp content was handwritten.
    - Some of it was difficult to read due to scan quality.
  - Document AI still extracted relevant information, including:
    - Quantities
    - Descriptions
    - Unit price
    - Total amounts
  - Some stamp information was included in the description column, but it did not interfere with the rest of the extracted data.
  - For invoices, **key value extraction was not applied** in this case.

## Important Terms
- **Document AI**: A service used for working with document images.
- **Text Extraction**: The process of extracting raw text content from images.
- **Key Value Extraction**: Identifying predefined keys (like merchant name or transaction date) and assigning corresponding values.
- **Line Item Data**: Structured details of purchased items, such as product names.
- **Tabular Data**: Extracted information organized in table format (e.g., quantities, descriptions, prices).
- **Stamp**: Additional markings or handwritten notes applied to documents after processing.

## Summary
Document AI successfully processes receipts and invoices by extracting raw text, key values, line items, and tabular data.  
- For receipts, it identifies specific keys and values, along with itemized purchases.  
- For invoices, it extracts all text and structured data, even handling partially legible handwritten or stamped information without disrupting other extracted details.  
