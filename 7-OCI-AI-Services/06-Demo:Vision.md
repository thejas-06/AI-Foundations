# OCI Vision Console Walkthrough - Learning Notes

## Overview
This lesson demonstrates the use of **OCI Vision** in the console. It covers navigating to the Vision service, exploring available resources, exercising features like image classification and object detection, and understanding how results are tagged, bounded, and detected in various scenarios.

## Key Concepts
- **OCI Vision Console**: Access point for Vision features from the OCI console under Analytics and AI.
- **Image Classification**: Assigns descriptive tags to entire images based on their content.
- **Object Detection**: Identifies specific objects within an image, applies bounding boxes, and tags them.
- **Default Images**: Preloaded images in the console to quickly test Vision’s features.
- **Custom Models**: A feature for building user-defined detection models (not demonstrated in this walkthrough).

## Detailed Notes
- **Navigation**:
  - Start from the OCI console homepage.
  - Navigate to **Analytics and AI → Vision**.
  - On the Vision homepage, a number of resources are available for exercising service features.

- **Features Available**:
  - **Image Analysis**: Through **image classification** or **object detection**.
  - **Document AI**.
  - **Custom Models**: Option to create, though not covered in this session.

- **Image Classification**:
  - Service includes default images for testing.
  - Example 1:
    - Tags: *overhead power line, transmission tower, plant, sky, line*.
    - Shows accurate classification of elements.
  - Example 2:
    - Uploaded image of iconic London landmarks.
    - Tags: *skyscraper, water, building, bridge, boat*.
    - All tags are appropriate for the scene.

- **Object Detection**:
  - Uses default images initially.
  - Detects specific objects and places bounding boxes around them.
  - **Example Scene**:
    - Objects detected:
      - Front center: *car*.
      - Back: *bus*.
      - Sidewalk: *people*.
      - Another *car* partially visible.
    - Text detected:
      - *License plate*.
      - *Oracle logo* on a car.
      - *Bus route* (detected even when difficult to read).
      - *Advertisement* on a cab.
      - Route details on a bus in the background.

  - **Low-Resolution Image Example**:
    - Detected: *person* standing on a roof.
    - Not detected: *microwave transmission antennas* (circular objects).
    - Explanation: Model not trained to detect these.
    - Custom models could be built to detect such objects.

  - **Cyclists Scene Example**:
    - Detects *person*, even when hunched and facing away.
    - Detects *bicycle* with nested bounding boxes (e.g., bicycle and wheel).
    - Further away, still detects another person on a bicycle.
    - Minimal text detected: only what appears as a dash on clothing.

## Summary
The **OCI Vision console** enables quick exploration of image analysis features.  
- **Image classification** assigns meaningful tags to entire images.  
- **Object detection** identifies individual objects, places bounding boxes, and recognizes even small details, including text like logos, license plates, and advertisements.  
- Detection accuracy can vary based on training; unusual objects may require custom models.  
Through various examples, Vision demonstrates strong capabilities in recognizing scenes, objects, people, vehicles, bicycles, and text in diverse images.
