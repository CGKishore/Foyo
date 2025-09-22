# Foyo
#### A fine tune object detection model using Falcon Duality AI synthetic data

This repository contains a custom YOLOv11s object detection model fine-tuned to detect 7 safety-related objects:
OxygenTank, NitrogenTank, FirstAidBox, FireAlarm, SafetySwitchPanel, EmergencyPhone, FireExtinguisher

The following sections describe how to train and evaluate the model step by step.

## 🚀 Model Training Process

### Environment Setup

- Use Google Colab with GPU support for efficient YOLO fine-tuning.

### Dataset Preparation

- Upload the training dataset ZIP folder to Google Drive.

- Extract the dataset in Colab.

- Create a YAML configuration file specifying paths for train, validation,      and test datasets and class names.

### YOLOv11s Model Setup

- Use the pre-trained YOLOv11s model as a starting point for fine-tuning.

### Training Parameters

- Set epochs, batch size, patience, learning rate, and optimizer in your       training script.

- Apply data augmentation techniques (flip, scale, mosaic, blur, etc.) to      improve performance.

### Start Training

- Run your training script (model training) in Colab.

- Monitor the training progress and visualizations for loss and accuracy.

### Save the Model

- Save the trained weights and run logs to Google Drive for evaluation and     deployment.

## 📊 Model Evaluation Process

### Evaluation Environment

- Use local Jupyter Notebook or any Python environment for evaluation.

- GPU is not required for inference.

### Load Trained Model

- Load the saved YOLOv11s model weights from Google Drive.

### Prepare Test Dataset

- Ensure the test dataset path and class info are correctly specified in the    YAML file.

### Run Evaluation

- Execute the evaluation script to compute predictions and performance         metrics.

- Inspect outputs such as predicted images, logs, and confusion matrix for     analysis.

## 💡 Notes for Users

- All scripts and configuration files are included in the repository.

- Following this guide, anyone can reproduce the training and evaluation       results easily.

- Always adjust paths in the YAML file according to your environment before    running scripts.
