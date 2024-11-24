# Brain Tumor Detection
This project uses a deep learning model for brain tumor detection based on magnetic resonance imaging (MRI). The notebook Brain_Tumor_Detection.ipynb contains all the code necessary to train and evaluate the model.

## Project Overview

This project consists of three main parts:

1. **Data Preprocessing**:
    - **Splitting the Data**: The images are divided into training, validation, and test sets.
    - **Cropping**: A crop is applied to the images.
    - **Resizing**: The images are resized to a standard dimension.
    - **Data Augmentation**: Various data augmentation techniques are applied to increase the diversity of the dataset.

2. **Neural Network Construction**:
    - **Transfer Learning**: The neural network is built using transfer learning, specifically employing the ResNet50 architecture.

3. **Testing Phase**:
    - **Model Testing**: The trained model is tested to evaluate its performance.
  
## Prerequisites

To automatically download the zip file of the dataset, you will need:


  - A Kaggle account, sign up on [Kaggle](https://www.kaggle.com/).
  - Go to your Kaggle account and create your API token.
  - Download the kaggle.json file which contains your authentication token.
  - Upload the kaggle.json file to the Colab runtime before running the notebook. This is necessary to download the dataset from Kaggle.

## Requirements

- Python 3.x
- Jupyter Notebook
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- OpenCV

## Architecture

The architecture of the network includes:

1. **Input Layer**: Accepts images resized to 224x224 pixels.
2. **Pre-trained Base Model**: The ResNet50 model pre-trained on the ImageNet dataset is used as the base. This model includes:
    - Convolutional layers that extract features from the input images.
    - Batch normalization and activation layers to stabilize and enhance training.
    - Residual blocks to allow for deeper networks by alleviating the vanishing gradient problem.
3. **Global Average Pooling Layer**: Reduces the spatial dimensions of the feature maps from the base model, providing a 1D feature vector.
4. **Dropout Layer**: A dropout layer with a dropout rate of 0.2 to prevent overfitting.
5. **Output Layer**: A dense layer to output the prediction.
