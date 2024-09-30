# AI4ALL Project: Wildfire Prediction

## Overview
This project explores wildfire detection using machine learning and convolutional neural networks (CNNs), focusing on binary image classification. We applied pre-trained models like ResNet50 and Inception-ResNet-V2 to classify outdoor images as either containing fire or not, fine-tuning them to our dataset. The project has applications in early wildfire detection, contributing to improved safety and environmental monitoring systems.

## Research Question

How can machine learning techniques be leveraged to classify outdoor images as fire or non-fire to enhance wildfire monitoring systems for improved safety and alertness?

## Dataset

We used two datasets, both sourced from Kaggle:

- FIRE Dataset (from the NASA Space Apps Challenge).
  - Used to train a model that can recognize images with fire.
  - Contains a mix of fire and non-fire images.
- Wildfire Detection Image Dataset:
  - This dataset was incorporated to address the class imbalance in the original dataset.
  - Additional non-fire images were added to improve the classification process.


## Model and Infrastructure

- We implemented two deep learning models:
  - ResNet50: Accuracy of 75% with a perfect recall of 1.00.
  - Inception-ResNet-V2: Achieved 94% accuracy and was selected as the better performing model.

- Infrastructure:
  - Code was developed using Google Colab, TensorFlow, and Keras.
  - Data preprocessing involved image normalization (rescaling pixel values to the range 0-1).


## Key Features

- Adversarial Testing: The model was tested on challenging images like campfires, candles, and sunsets to assess its robustness.
- Model Training:
  - Training size: 799 images
  - Validation size: 101 images
  - Testing size: 99 images
- Model Outputs: The models classify images as fire or non-fire based on binary classification techniques.

## Results

- ResNet50 achieved a recall of 1.00, making it a great choice for minimizing false negatives (i.e., not missing any fire incidents).
- Inception-ResNet-V2 was more accurate overall, making it the best-performing model for general use.

## Ethical Considerations

We considered the following ethical implications during the development process:

- Algorithmic Bias: The model might be biased based on the limited dataset, and further improvements in data diversity are needed.
- Data Privacy: Care was taken to ensure the datasets used are open-source and do not violate privacy concerns.

## Challenges

- GPU Limitations: Some team members faced difficulties running the model due to GPU constraints.
- Dataset Imbalance: Initially, the dataset contained an imbalance between fire and non-fire images, which was addressed by adding more non-fire images.

## Future Work
- Explore real-time fire detection and integrate the model into a monitoring system for rapid response.
- Further development of wildfire detection models could focus on predicting the spread of fires using geospatial data to enable better emergency response planning and resource allocation.
- We also aim to address algorithmic bias by collecting more diverse datasets from various global environments.
  
