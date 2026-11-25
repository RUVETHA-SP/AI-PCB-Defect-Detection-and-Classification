# AI-PCB-Defect-Detection-and-Classification

📌 Overview

Printed Circuit Board (PCB) inspection is an important step in electronics manufacturing. Manual inspection can be time-consuming and may be affected by human error.

This project explores an automated approach for identifying PCB defects using computer vision and deep learning.

The system takes a PCB image as input, processes the image, and predicts whether a defect is present and, where applicable, identifies the defect category.
___________________________________________________________________________________________________________________________________________________________________
🎯 Problem Statement

Manual PCB inspection requires significant time and attention, particularly when inspecting a large number of boards.

The objective of this project is to develop an AI-based system that can:

•  Automatically analyze PCB images

•  Detect defective regions

•  Classify PCB defects

•  Reduce dependence on manual visual inspection

•  Provide consistent inspection results
_______________________________________________________________________________________________________________________________________________________________     
🚀 Project Objectives

The main objectives of this project are:

- Detect defects in PCB test images using a defect-free reference image.
- Identify and localize defective regions.
- Extract individual defect regions using image processing techniques.
- Classify detected defects using a deep learning model.
- Develop a user-friendly web interface for PCB inspection.
- Display detected defects with bounding boxes and labels.
- Generate annotated output images and prediction logs.
________________________________________________________________________________________________________________________________________________________________ 🧠Model Training and Performance

The system uses **EfficientNetB0**, a transfer learning-based deep learning architecture, for PCB defect classification.

The model was trained and evaluated using a PCB defect image dataset.

### Evaluation Results

| Metric | Result |
|---|---:|
| Test Accuracy | 96.30% |
| Test Loss | 0.0982 |
| Test Samples | 460 |

### PCB Defect Categories

The model classifies six types of PCB defects:

- Missing Hole
- Mouse Bite
- Open Circuit
- Short
- Spur
- Spurious Copper

### Evaluation Outputs

- Classification Report
- Confusion Matrix
- Class-wise Precision, Recall and F1-score

**Note:** The reported accuracy represents the model's test-set classification performance.
