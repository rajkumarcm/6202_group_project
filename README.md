# Analyzing the Robustness of Transfer Learning in Brain Tumor Diagnosis

## Overview

-Compares two self-built CNN models against a fine-tuned pre-built model EfficientNetV2B2.  
-All three models performed above 0.9 measured using F1-macro score. While comparing under cases when a set of images with common postures is presented to both the networks, self-built model performed better than the pre-trained model.  
-The [Br35H :: Brain Tumor Detection 2020](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection) Kaggle data set was used to train and do inital testing of the models.  
-The [Brain Tumor Classification (MRI)](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri?select=Training) Kaggle data set was used to retest the models on brain scan data with new orientations.

## Results on Initial Test Set

### Self-Built Small-Scale Convolution Neural Network  
-*accuracy*: 0.9300  
-*macro F1*: 0.9344  

### Self-Built Large-Scale Residual Neural Network
-*accuracy*: 0.9400  
-*macro F1*: 0.9432  

### Pretrained Model Based on EfficientNetV2B2
-*accuracy*: 0.9233  
-*macro F1*: 0.9235  

## Conclusions

1. Residual Network is an architecture that is robust to training large-scale neural networks.  
2. Once the data is expected to have many layers to achieve good performance, residual blocks can be used to ensure the gradient flow to earlier layers is unhindered.  
3. Despite the complexity of the pre-built model, training both the network with same set of images, the pre-trained model was unable to outperform the self-built Residual based CNN model.  
