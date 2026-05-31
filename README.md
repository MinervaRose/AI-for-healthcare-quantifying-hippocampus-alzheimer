# 🧠 AI for Healthcare: Quantifying Alzheimer's Disease Progression Through Hippocampal Volume Analysis

### Medical Imaging • MRI Segmentation • U-Net • DICOM Integration • Clinical AI

![Python](https://img.shields.io/badge/Python-Medical_AI-blue?style=for-the-badge\&logo=python\&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-U--Net-orange?style=for-the-badge\&logo=pytorch\&logoColor=white)
![MONAI](https://img.shields.io/badge/MONAI-Medical_Imaging-red?style=for-the-badge)
![MRI](https://img.shields.io/badge/MRI-Brain_Imaging-purple?style=for-the-badge)
![DICOM](https://img.shields.io/badge/DICOM-Clinical_Workflows-green?style=for-the-badge)

---

# Overview

This project explores the use of deep learning and medical imaging workflows to automatically segment the hippocampus from brain MRI scans and estimate hippocampal volume.

Hippocampal atrophy is a well-established biomarker associated with Alzheimer's Disease and other neurodegenerative disorders. Manual measurement is time-consuming and requires expert radiological interpretation.

The goal of this project was to build an end-to-end AI workflow capable of:

* Curating MRI datasets
* Training a segmentation neural network
* Quantifying hippocampal volume
* Integrating inference into a simulated clinical imaging environment

---

# Why Hippocampal Volume Matters

The hippocampus plays a central role in:

* Memory formation
* Learning
* Spatial navigation

Numerous studies have demonstrated that hippocampal volume decreases as Alzheimer's Disease progresses.

Automated segmentation systems can help:

* Reduce clinician workload
* Improve measurement consistency
* Enable longitudinal disease monitoring
* Support clinical research

---

# Project Structure

This project is organized into three major sections.

## Section 1 — MRI Dataset Curation & Exploration

### Objectives

* Inspect NIfTI MRI volumes
* Analyze metadata
* Identify and remove problematic files
* Understand voxel dimensions and physical volume measurements
* Visualize anatomical structures

### Activities

* MRI slice visualization
* Voxel dimension analysis
* Hippocampal volume histograms
* Outlier detection and removal
* Dataset quality assessment

### Key Concepts

* NIfTI imaging
* Voxel spacing
* Anatomical volume estimation
* Medical image preprocessing

---

## Section 2 — Deep Learning Segmentation

### Objective

Train a convolutional neural network capable of segmenting the hippocampus from MRI scans.

### Architecture

Modified U-Net implemented with:

* PyTorch
* MONAI
* Dice Loss

### Training Pipeline

```text
MRI Volume
     │
     ▼
Preprocessing
     │
     ▼
Slice Extraction
     │
     ▼
U-Net Segmentation
     │
     ▼
Predicted Mask
     │
     ▼
Volume Calculation
```

### Monitoring

Training was monitored using TensorBoard.

Tracked metrics included:

* Training loss
* Validation loss
* Predicted masks
* Ground-truth masks
* Probability maps

### Segmentation Metrics

Evaluation used volumetric segmentation metrics:

* Dice Score
* Jaccard Index
* Sensitivity
* Specificity

---

## Section 3 — Clinical Workflow Integration

### Objective

Deploy the segmentation model into a simulated clinical environment.

### Components

#### Orthanc PACS

Stores incoming imaging studies.

#### DICOM Routing

Automatically routes MRI studies to the AI module.

#### Segmentation Engine

Processes incoming studies and generates volume measurements.

#### OHIF Viewer

Displays imaging studies and generated reports.

### Clinical Pipeline

```text
MRI Scanner
      │
      ▼
Orthanc PACS
      │
      ▼
AI Segmentation Module
      │
      ▼
Volume Report
      │
      ▼
OHIF Viewer
      │
      ▼
Radiologist Review
```

---

# Model Performance

The segmentation model achieved strong overlap between predicted and annotated hippocampal regions.

Representative validation results included:

* Dice Score ≈ 0.86
* Jaccard Score ≈ 0.76
* Sensitivity ≈ 0.88
* Specificity ≈ 0.95

These metrics indicate accurate anatomical segmentation under the project evaluation framework.

---

# TensorBoard Monitoring

Training was monitored through TensorBoard visualizations including:

* Training and validation loss curves
* Input MRI slices
* Ground-truth masks
* Predicted masks
* Probability overlays

This ensured visibility into convergence behaviour and model performance.

---

# Clinical Validation Planning

A formal validation plan was created covering:

* Intended clinical use
* Ground truth generation
* Dataset collection methodology
* Performance assessment
* Clinical deployment considerations
* Validation cohort design

This mirrors the types of planning required for real-world medical AI deployment.

---

# Repository Contents

```text
section1/
│
├── MRI Dataset Exploration
├── Volume Analysis
└── EDA Notebook

section2/
│
├── U-Net Training
├── TensorBoard Monitoring
├── Model Checkpoints
└── Segmentation Evaluation

section3/
│
├── DICOM Inference
├── Orthanc Integration
├── OHIF Visualization
└── Clinical Reporting

reports/
│
├── Validation Plan
├── Training Optimization Report
├── Clinician Summary
└── TensorBoard Results
```

---

# Skills Demonstrated

## Medical Imaging

* MRI analysis
* NIfTI processing
* DICOM workflows
* Anatomical segmentation

## Deep Learning

* U-Net architecture
* Semantic segmentation
* PyTorch
* MONAI

## Clinical AI

* PACS integration
* Orthanc deployment
* OHIF reporting
* Validation planning

## Evaluation

* Dice coefficient
* Jaccard index
* Volume estimation
* Model monitoring

---

# Key Deliverables

* MRI dataset exploration notebook
* Segmentation training pipeline
* Trained U-Net model
* TensorBoard monitoring outputs
* Clinical validation plan
* Clinician-facing summary report
* DICOM inference workflow
* OHIF-compatible reporting system

---

# Educational Context

This project was completed as part of the AI for Healthcare Nanodegree and demonstrates the complete lifecycle of a medical imaging AI system:

Dataset → Model → Validation → Clinical Integration

---

## Author

S. Palis

AI Systems • Medical Imaging • Healthcare AI • Clinical Decision Support
