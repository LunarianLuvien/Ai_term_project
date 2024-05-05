# Object Detection and Image Processing Pipeline

This project involves a comprehensive pipeline for object detection in images, using a neural network to detect specific objects and applying image processing techniques to manipulate the detected regions. The system is implemented using Python and leverages libraries such as OpenCV, Pandas, and TensorFlow.

## Overview
The project processes images to detect defined objects using bounding boxes. The detected objects can then be manipulated, such as obscuring them in the image. The system also involves training a model to improve accuracy in object detection.

## Pipeline Stages
1. **XML Parsing and CSV Conversion:**
   - Extracts data from XML files, which include bounding box coordinates.
   - Data is parsed using `xml.etree.ElementTree` and stored in a Pandas DataFrame, then saved as a CSV for easier access.

2. **Image Data Preparation:**
   - Reads image file paths from the CSV.
   - Images and their corresponding bounding boxes are loaded and pre-processed, including resizing and normalization.

3. **Model Training:**
   - Uses pre-trained models like InceptionResNetV2 from TensorFlow with transfer learning to detect bounding boxes around objects.
   - The model is trained with images and their bounding box coordinates, adjusting to accurately predict object locations.

4. **Object Detection on New Images:**
   - Performs object detection on new images using the trained model.
   - Detected bounding boxes are used to manipulate the image, such as drawing rectangles around detected objects or obscuring them.

5. **Image Manipulation:**
   - Applies various image manipulations based on the detected objects, such as creating a black image with a white rectangle in the region of the detected object.

## Tools and Technologies
- **Python:** For scripting and handling data.
- **OpenCV:** Used for image processing tasks.
- **Pandas:** For data manipulation and storage.
- **TensorFlow:** To train and utilize neural network models for object detection.
- **Matplotlib:** For displaying images.

## Execution Details
The pipeline consists of multiple Python scripts that:
- Parse XML data to extract bounding box coordinates.
- Pre-process image data for neural network input.
- Train a neural network to recognize and predict bounding boxes.
- Use the model to detect objects in new images and manipulate these images based on detection results.

## How to Run
1. Ensure all dependencies are installed using pip.
2. Run the script to parse XML and prepare data.
3. Train the model with prepared data.
4. Apply the model to new images for object detection and subsequent image manipulation.
