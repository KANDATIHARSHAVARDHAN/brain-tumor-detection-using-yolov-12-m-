# Brain Tumor Detection Using YOLOv12

This repository contains a machine learning project that uses YOLOv12 for detecting and classifying brain tumors in MRI scans.

## Overview

The project implements an object detection model to identify and classify brain tumors into four categories:
- Glioma
- Meningioma
- No Tumor
- Pituitary

The model is trained on a dataset of MRI scans and can process both images and videos for tumor detection.

## Model Performance

The trained model achieved impressive metrics:

| Class        | Images | Instances | Box(P) | R     | mAP50 | mAP50-95 |
|-------------|--------|-----------|--------|-------|-------|----------|
| All Classes | 496    | 541       | 0.928  | 0.922 | 0.96  | 0.784    |
| Glioma      | 135    | 153       | 0.909  | 0.85  | 0.923 | 0.735    |
| Meningioma  | 134    | 136       | 0.98   | 0.971 | 0.991 | 0.831    |
| No Tumor    | 91     | 91        | 0.967  | 0.966 | 0.992 | 0.828    |
| Pituitary   | 154    | 161       | 0.855  | 0.901 | 0.934 | 0.741    |

### Key Performance Indicators:
- **mAP50**: 0.96 (Mean Average Precision at 50% IoU threshold)
- **mAP50-95**: 0.784 (Mean Average Precision across multiple IoU thresholds)
- **Precision**: 0.928 overall with highest precision for Meningioma class (0.98)
- **Recall**: 0.922 overall with highest recall for No Tumor class (0.966)

## Project Structure

- **Data Preparation**: Custom dataset of brain MRI scans with annotations
- **Model Training**: YOLOv12 model trained for 30 epochs with batch size of 15
- **Evaluation**: Comprehensive metrics calculation on validation dataset
- **Inference**: Capability to analyze both static MRI images and MRI videos

## Features

- Detection and classification of multiple tumor types in a single scan
- Real-time tumor detection in MRI video sequences
- High precision identification of tumor boundaries
- Confidence scoring for each detection
- Support for different input formats (JPEG, PNG, MP4)

## Applications

- Medical diagnosis assistance
- Tumor region localization
- Training tool for medical professionals
- Research on brain tumor characteristics
- Patient education on tumor location and type

## Requirements

- Ultralytics YOLOv12
- OpenCV
- Matplotlib
- PIL (Python Imaging Library)
