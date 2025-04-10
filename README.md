# Alzheimer's Disease Classification

This repository uses [Augmented Alzheimer MRI Dataset](https://www.kaggle.com/datasets/uraninjo/augmented-alzheimer-mri-dataset). In this notebook, a VGG16 model is used here to classify brain MRIs into normal, very-mild, mild and moderate Alzheimer classes.

The lack of important parameters such as data source, unique id of patients, patient id of slices taken from 3D images and patient splitting method makes the used Kaggle data set unusable for research. One of the most important concept to consider for deep learning in medical research is the appropriate train-test splitting of patient data due to leakage concerns.

Kaggle baseline data set contains total 6.400 2D slices with unknown location includes 896 Mild Demented, 64 Moderate Demented, 3.200 Non-Demented and 2.240 Very Mild Demented subjects.
Kaggle augmented data set contains total 33.984 samples with 8.960 Mild Demented, 6.464 Moderate Demented, 9.600 Non-Demented and 8.960 Very Mild Demented subjects. Augmented data set employed as training set and baseline utilized as test set to simulate common wrong applications in the literature.


# Workflow Documentation

The `augmented-alzheimer-mri` notebook is structured to analyze and classify MRI images for Alzheimer's disease detection. It includes data preprocessing, visualization, model training, evaluation, and explainability. The workflow is divided into the following sections:

1. **Dataset Preparation**: Loading and organizing the dataset into augmented and original categories.
2. **Dataset Analysis**: Visualizing the distribution of classes to identify any imbalances.
3. **Data Visualization**: Displaying random images from the dataset to understand the data better.
4. **Data Processing**: Splitting the dataset into training, validation, and testing sets, and resizing images for model input.
5. **Model Training**: Using pretrained models like VGG16 and ResNet50 for classification.
6. **Model Evaluation**: Comparing models based on metrics like F1 score, AUC, and accuracy.
7. **Explainability**: Visualizing the regions of the brain contributing to model predictions using gradient-based methods.
8. **Model Saving and Loading**: Saving trained models for future use and reloading them for evaluation or inference.