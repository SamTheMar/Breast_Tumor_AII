# Breast_Tumor_AII

The idea of this project is create is a ML and a DL model capable to detect and classify Breast Tumor given an image as input.

## Data

The original dataset [`Dataset_BUSI_with_GT`] is composed by 3 subfolder representing the class (normal, malignant, benign). Each of that folder contains the original images and the masks (ground truth).

## Machine Learning model
For the ML model first of all we extract important features with computer vision techniques [`FeaturesExtraction.ipynb`] and save as `csv` file [`Features.csv`], then we try different resampling techniques and ML models [`Classification_ML.ipynb`] in order to achieve a better results.

## Deep Learning model
The main idea for the DL model is create something that can gives a visual help to doctors. This it the reason why we use a segmentation model. We try train the model with a weighted class loss [`breast-cancer-segmentation_class_weighted.ipynb`] and without [`breast-cancer-segmentation_unweighted.ipynb`].

## Metrics
For all the model tested we use as metrics:
- precision macro
- recall macro
- f1 macro

## Results
### ML model
- precision macro 79.41
- recall macro 80.10
- f1 macro 79.53
### DL model
- precision macro 0.81
- recall macro 0.82
- f1 macro 0.81