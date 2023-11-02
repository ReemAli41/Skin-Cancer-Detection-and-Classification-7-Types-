# Skin Cancer Detection and Classification
![Skin Cancer](Skin-Cancer-Detection-and-Classification-7-Types-
/1.PNG)

## Table of Contents

- [Introduction](#introduction)
- [Project Idea](#project-idea)
- [Data and its Problems](#data-and-its-problems)
- [Image Preprocessing](#image-preprocessing)
- [Data Augmentation](#data-augmentation)
- [Hair Remover](#hair-remover)
- [Splitting Data](#splitting-data)
- [Normalization](#normalization)
- [Models and Results](#models-and-results)
- [Website](#website)

## Introduction

Skin cancer is a significant public health concern, with a rising incidence of cases and a lack of awareness regarding symptoms and prevention. This project aims to address this issue by developing a skin cancer detection and classification system that can identify the seven most common types of skin cancer: Basal cell carcinoma, Actinic keratosis, Melanoma, Nevus, Vascular lesion, Squamous cell carcinoma, and Pigmented benign keratosis.

## Project Idea

Skin cancer is a growing health concern with a higher incidence rate than several other types of cancer, such as breast, prostate, lung, and colon cancer combined. The primary objective of this project is to create a framework for analyzing and assessing the risk of melanoma using dermoscopic images. This system will assist specialists in faster and more accurate classification of skin cancer types.

## Data and Its Problems

The project utilized the ISIC Skin Cancer dataset from Kaggle. The primary challenges with the dataset were its unbalanced nature and relatively small size, making it challenging to work with effectively without image cleaning and preprocessing.

### Data Before Applying Cleaning and Preprocessing

| Class Label | Class Name             | Count Before Augmentation |
|-------------|------------------------|---------------------------|
| 0           | Actinic Keratosis      | 144                       |
| 1           | Basal Cell Carcinoma   | 376                       |
| 2           | Melanoma               | 438                       |
| 3           | Nevus                  | 357                       |
| 4           | Pigmented Benign Keratosis | 462                   |
| 5           | Squamous Cell Carcinoma | 181                      |
| 6           | Vascular Lesion        | 139                       |

## Image Preprocessing

The following image preprocessing steps were applied to address data issues and improve model performance:

- **Image Resize**: Images were resized to a consistent dimension.
- **Data Augmentation**: Augmentation techniques were applied using Keras' ImageDataGenerator, including shifting, rotation, flipping, shearing, and zooming.

## Data Augmentation

Class labels were balanced by applying data augmentation, resulting in the following counts after augmentation:

| Class Label | Class Name             | Count After Augmentation |
|-------------|------------------------|---------------------------|
| 0           | Actinic Keratosis      | 2500                      |
| 1           | Basal Cell Carcinoma   | 2500                      |
| 2           | Melanoma               | 2500                      |
| 3           | Nevus                  | 2500                      |
| 4           | Pigmented Benign Keratosis | 2500                  |
| 5           | Squamous Cell Carcinoma | 2500                      |
| 6           | Vascular Lesion        | 2500                      |

## Hair Remover

An attempt was made to remove hair from images using a hair remover function with a Gaussian filter. However, it did not significantly impact the results or accuracy.

## Splitting Data

Data was split into training and testing sets using the `train_test_split()` function.

## Normalization

Data was normalized to ensure that all input features were on a similar scale.

## Models and Results

Various machine learning models were evaluated, including SVM, ResNet-50, VGG16, InceptionV3, and DenseNet-201. DenseNet-201 demonstrated the best accuracy at 93%.

## Website

The skin cancer detection and classification model was deployed using Flask, and a website was developed with HTML and CSS to provide a user-friendly interface for using the model.

