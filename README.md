# Syook Person and PPE Detection model.

This project implements a two-stage detection system using YOLOv8 models for person detection in full images and PPE detection on cropped person images.

## Features

- Convert Pascal VOC annotations to YOLOv8 format
- Person detection using YOLOv8
- PPE detection on cropped person images
- Support for multiple PPE classes (hard-hat, gloves, mask, glasses, boots, vest, etc.)
- Visualization of detection results
- Flexible data processing pipeline for model training

## Prerequisites

- Python 3.8+
- GPU (recommended for faster training and inference)
- Jupyter notebook

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/srivastavaarpit977/Syook-Person-and-PPE-Detection-Model.git
   

2. Install the required packages:
   ```sh
   pip install ultralytics opencv-python argparse lxml

## Overview of the Process

### 1. Dataset Preparation

**Person Detection:**

- The dataset was initially filtered to focus on detecting persons.
- Images and labels were divided into `train`, `valid`, and `test` subfolders.

**PPE Detection:**

- After training the person detection model, the images were cropped to isolate detected persons.
- These cropped images were then organized similarly into `train`, `valid`, and `test` subfolders for PPE detection training.

### 2. Training and Inference

**Person Detection Model:**

- The filtered dataset was used to train the person detection model.

**PPE Detection Model:**

- The cropped images, focused on persons, were used to train the PPE detection model.

**Inference:**

- The `inference.py` script was then used to detect persons first and subsequently detect PPE on the cropped images.

### 3. Labeling Issues

- During the training of the PPE detection model, some class labels were incorrectly labeled, causing warnings and leading to inaccuracies in the model’s detection of PPE.
- This issue highlighted the importance of correct labeling for effective model performance.

## Conclusion

This process demonstrates the importance of correctly preparing datasets and labeling to ensure effective model training and accurate detection results.

