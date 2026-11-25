# AI-PCB-Defect-Detection-and-Classification

## 📌 Overview

Printed Circuit Board (PCB) inspection is an important step in electronics manufacturing. Manual inspection can be time-consuming and may be affected by human error.

This project explores an automated approach for identifying PCB defects using computer vision and deep learning.

The system takes a PCB image as input, processes the image, and predicts whether a defect is present and, where applicable, identifies the defect category.
___________________________________________________________________________________________________________________________________________________________________
## 🎯 Problem Statement

Manual PCB inspection requires significant time and attention, particularly when inspecting a large number of boards.

The objective of this project is to develop an AI-based system that can:

•  Automatically analyze PCB images

•  Detect defective regions

•  Classify PCB defects

•  Reduce dependence on manual visual inspection

•  Provide consistent inspection results
_______________________________________________________________________________________________________________________________________________________________     
## 🚀 Project Objectives

The main objectives of this project are:

- Detect defects in PCB test images using a defect-free reference image.
- Identify and localize defective regions.
- Extract individual defect regions using image processing techniques.
- Classify detected defects using a deep learning model.
- Develop a user-friendly web interface for PCB inspection.
- Display detected defects with bounding boxes and labels.
- Generate annotated output images and prediction logs.
_________________________________________________________________________________________________________________________________________________________
 ## 🧠 Model Training and Performance

The system uses **EfficientNetB0**, a transfer learning-based deep learning architecture, for PCB defect classification.

The model was trained and evaluated using a PCB defect image dataset.

## Evaluation Results

| Metric | Result |
|---|---:|
| Test Accuracy | 96.30% |
| Test Loss | 0.0982 |
| Test Samples | 460 |

## PCB Defect Categories

The model classifies six types of PCB defects:

- Missing Hole
- Mouse Bite
- Open Circuit
- Short
- Spur
- Spurious Copper

 ## Evaluation Outputs

- Classification Report
- Confusion Matrix
- Class-wise Precision, Recall and F1-score

**Note:** The reported accuracy represents the model's test-set classification performance.

___________________________________________________________________________________________________________________________________________________________________
## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| OpenCV | Image processing and defect extraction |
| TensorFlow | Deep learning model development |
| EfficientNetB0 | Transfer learning-based defect classification |
| NumPy | Numerical operations and image array processing |
| DeepPCB | PCB defect image dataset |

### Development Tools
- Visual Studio Code
- Python Virtual Environment
- Git and GitHub

  ___________________________________________________________________________________________________________________________________________________________________
## 🏗️ System Architecture

The proposed system follows an image-processing and deep-learning-based workflow to detect and classify PCB defects.

### Workflow

1. **Input Images:** Provide the PCB test image and defect-free template image.
2. **Image Subtraction:** Compare the test image with the reference template to identify differences.
3. **Otsu Thresholding:** Convert the difference image into a binary defect mask.
4. **Morphological Operations:** Apply erosion and dilation to improve defect regions.
5. **Contour Extraction:** Identify defect boundaries and extract individual Regions of Interest (ROI).
6. **Model Training:** Train the EfficientNetB0 model using labeled PCB defect images.
7. **Defect Classification:** Classify extracted defect regions into predefined categories.
8. **Output:** Generate defect classification results and visualizations.

### System Workflow

```text
PCB Test Image + Template Image
              |
              v
       Image Subtraction
              |
              v
       Otsu Thresholding
              |
              v
     Erosion and Dilation
              |
              v
       Contour Extraction
              |
              v
        ROI Extraction
              |
              v
     EfficientNetB0 Model
              |
              v
      Defect Classification
              |
              v
       Prediction Results
```

The system combines traditional computer vision techniques with deep learning to support automated PCB defect inspection.

___________________________________________________________________________________________________________________________________________________________________
## 🔍 Image Processing Techniques

The system uses OpenCV-based image processing techniques to identify and extract defective regions from PCB images.

### 1. Image Subtraction
Compares the PCB test image with a defect-free reference template to identify differences that may indicate defects.

### 2. Otsu Thresholding
Applies automatic threshold selection to convert the difference image into a binary image, highlighting potential defect regions.

### 3. Erosion and Dilation
Uses morphological operations to remove small unwanted noise and refine the detected defect regions.

### 4. Contour Extraction
Identifies the boundaries of detected regions to locate potential PCB defects.

### 5. Region of Interest (ROI) Extraction
Extracts individual defect regions from the PCB image for further analysis and classification.

### Tools Used
- OpenCV
- NumPy
- Python

___________________________________________________________________________________________________________________________________________________________________
## 📂 Dataset Description

This project uses the **DeepPCB Dataset** for PCB defect detection and classification.

The dataset contains PCB images used for image processing, defect region extraction, and deep learning-based classification.

### Dataset Organization

The dataset is organized into the following directories:

- `raw/` – Original dataset images.
- `train/` – Training images.
- `val/` – Validation images.
- `test/` – Testing images.
- `roi_dataset/` – Extracted defect regions (Regions of Interest).

### PCB Defect Categories

The trained EfficientNetB0 model classifies the following six PCB defect categories:

| No. | Defect Category |
|---|---|
| 1 | Missing Hole |
| 2 | Mouse Bite |
| 3 | Open Circuit |
| 4 | Short |
| 5 | Spur |
| 6 | Spurious Copper |

### Dataset Usage

- Training: Used to train the deep learning model.
- Validation: Used to monitor model performance during training.
- Testing: Used to evaluate the final model on test images.

The dataset is processed using image preprocessing and ROI extraction techniques before classification.

___________________________________________________________________________________________________________________________________________________________________
## 📊 Model Performance and Evaluation

The PCB defect classification model was developed using **EfficientNetB0** with transfer learning.

The model was evaluated on an independent test dataset to measure its classification performance.

### Test Results

| Evaluation Metric | Result |
|---|---:|
| Test Accuracy | 96.30% |
| Test Loss | 0.0982 |
| Test Samples | 460 |
| Defect Classes | 6 |

### Classification Evaluation

The model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### Model Evaluation Outputs

The following evaluation results were generated:

- Classification Report
- Confusion Matrix
- Class-wise Performance Metrics

The model achieved **96.30% test accuracy**, demonstrating strong classification performance across the six PCB defect categories.

