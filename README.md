# Foyo
A fine tune object detection model using Falcon Duality AI synthetic data

This repository contains a custom YOLOv11s object detection model fine-tuned to detect 7 safety-related objects:
OxygenTank, NitrogenTank, FirstAidBox, FireAlarm, SafetySwitchPanel, EmergencyPhone, FireExtinguisher.

The following sections describe how to train and evaluate the model.

🚀 Model Training Process

Environment Setup

Use Google Colab for GPU support, which is required for efficient YOLO fine-tuning.

Dataset Preparation

Upload your training dataset ZIP folder to Google Drive.

Extract it in Colab.

Prepare a YAML configuration file specifying the paths for training, validation, and testing datasets and class names.

YOLOv11s Model Setup

Start with the pre-trained YOLOv11s model to save training time and improve performance.

Training Parameters

Configure epochs, batch size, patience, learning rate, and optimizer in your training script.

Apply data augmentation techniques (optional but recommended for better performance).

Start Training

Run your training script (e.g., model training) in Colab.

Monitor training progress using the logs and visualization outputs.

Save the Model

After training, save the trained weights and run logs to Google Drive for later use.

📊 Model Evaluation Process

Evaluation Environment

Use local Jupyter Notebook or any Python environment for evaluation.

GPU is not required for inference.

Load Trained Model

Load the saved YOLOv11s model weights from your drive.

Prepare Test Dataset

Ensure the test dataset path and class info are correctly specified in the YAML configuration file.

Run Evaluation

Execute the evaluation script to compute predictions and performance metrics.

Inspect outputs such as predicted images, logs, or confusion matrix for analysis.
