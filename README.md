# Foyo
A fine tune object detection model using Falcon Duality AI synthetic data

This repository contains a custom YOLOv11s object detection model fine-tuned to detect 7 safety-related objects:
OxygenTank, NitrogenTank, FirstAidBox, FireAlarm, SafetySwitchPanel, EmergencyPhone, FireExtinguisher.

The following steps summarize the model training and evaluation process.

Model Training Process

Environment Setup:

Training was performed on Google Colab to leverage GPU support, which is required for fine-tuning YOLO models efficiently.

Dataset Preparation:

The training dataset was uploaded as a ZIP folder to Google Drive and extracted in Colab.

A YAML configuration file was created specifying paths for the training, validation, and test datasets, along with the class names.

YOLOv11s Model Setup:

The pre-trained YOLOv11s model was used as a starting point for fine-tuning.

This allowed faster convergence and better performance with a smaller dataset.

Training Parameters:

Epochs: 200 (training was stopped at 41 epochs due to Colab limits)

Batch Size: 32

Patience: 20

Learning Rate & Optimizer: Default YOLOv11s settings were used, as they are well-optimized for YOLO training.

Model Saving:

After training, the trained model weights and runs were saved to Google Drive for later evaluation and deployment.

Performance During Training:

The model achieved a mAP@0.5 of 0.744 on the validation dataset, demonstrating good detection and classification performance.

Training Notebook:

The complete training process is documented in the file model training uploaded in this repository.

Performance Evaluation Process

Evaluation Dataset:

The trained model was evaluated on the test dataset, which contains images not seen during training or validation.

Evaluation Environment:

Evaluation was performed locally using Jupyter Notebook on CPU.

GPU resources were not required as only inference and metric calculations were performed.

Evaluation Steps:

The trained model weights were loaded.

The test dataset paths and class information were provided through the YAML configuration file.

Model performance metrics were calculated, including mAP scores, precision, recall, F1-score, and confusion matrix analysis.

Evaluation Results:

mAP@0.5: 0.6312

mAP@0.5:0.95: 0.5066

Overall Precision: 0.8684

Overall Recall: 0.5565

Class-wise performance:

OxygenTank: 0.6505

NitrogenTank: 0.6168

FirstAidBox: 0.5951

FireAlarm: 0.4065

SafetySwitchPanel: 0.4220

EmergencyPhone: 0.3719

FireExtinguisher: 0.4836

Confusion Matrix Insights:

True Positives: High detection rates for dominant objects like OxygenTank and NitrogenTank.

False Negatives: Some small or occluded objects were missed (e.g., EmergencyPhone, FireAlarm).

False Positives: Misclassifications were low, indicating accurate predictions for most classes.

Success Cases:

Large and clear objects were detected accurately.

Failure Cases:

Small, occluded, or overlapping objects were sometimes missed or misclassified.

Inference Speed:

Preprocessing: 0.85 ms/image

Inference: 138.25 ms/image

Postprocessing: 1.63 ms/image

