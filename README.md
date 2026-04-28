# visual-triage-demo
This repository contains the Visual Triage (Skin Image Analysis) module developed as part of the CheckApp project.

The goal of this module is to classify skin lesion images into dermatological categories using deep learning and provide interpretable predictions using Grad-CAM.

This work is developed as a prototype system aligned with the project plan and is intended for research and educational purposes. 
Early experiments were conducted under different training conditions (different epoch counts).
Final comparisons should be performed under equal conditions for full fairness.

Two models are implemented and compared:

🔹 Baseline Model
ResNet-50
Used as a reference model
Provides a standard benchmark

🔹 Main Model
EfficientNet-B4
Selected as the primary model in the project plan
Trained using a multi-stage fine-tuning strategy:
Feature extraction
Partial unfreeze
Fine-tuning

## Dataset
HAM10000 (Human Against Machine with 10000 training images)
~10,000 dermoscopic images
7 skin lesion classes:
akiec
bcc
bkl
df
mel
nv
vasc

The dataset is highly imbalanced.
To address this:

Weighted loss functions are used
Evaluation includes F1-score metrics

 ## Evaluation Metrics

Models are evaluated using:

Accuracy
Precision / Recall
Macro F1-score
Weighted F1-score
Confusion Matrix

Accuracy alone is not sufficient due to class imbalance.

## Explainability (Grad-CAM)

Grad-CAM is used to improve interpretability:

Highlights image regions influencing predictions
Helps understand model behavior
Provides visual explanations for predictions

## Results & Outputs

Due to GitHub file size limitations, large output files and model checkpoints are not included in this repository.

The complete experimental notebook, training outputs, evaluation results, and generated visualizations can be accessed on Kaggle:

🔗 [Kaggle Notebook – CheckApp Visual Triage](https://www.kaggle.com/code/senademirba/project-sd)
