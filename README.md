# Architectural Style Classification Using Convolutional Neural Networks

## Overview

This project presents a Convolutional Neural Network (CNN) model designed to classify architectural styles from images.  
The model learns visual patterns and structural features specific to different architectural categories and predicts the class of unseen images.

This work demonstrates the application of deep learning and computer vision techniques in multi-class image classification.

---

## Objectives

- Develop a CNN-based image classification model
- Preprocess and organize architectural image datasets
- Split the dataset into training and validation sets
- Evaluate model performance using accuracy and loss metrics
- Perform predictions on new architectural images

---

## Dataset

The dataset is organized into directories, where each directory represents a specific architectural style:

Dataset/
│
├── Gothic/
├── Moorish/
├── Russian/
├── Amazigh/
├── Buddhist/
├── Egyptian/
└── ...

Each folder contains images corresponding to one architectural category.

The dataset is divided into:
- 80% training data
- 20% validation data

The split is performed programmatically using the `split-folders` library.

---

## Model Architecture

The CNN model is implemented using the Keras Sequential API.

Architecture:

- Conv2D (32 filters, ReLU activation)
- MaxPooling2D
- Conv2D (64 filters, ReLU activation)
- MaxPooling2D
- Conv2D (128 filters, ReLU activation)
- MaxPooling2D
- Flatten
- Dense (256 neurons, ReLU activation)
- Dropout (0.5)
- Dense (Softmax activation for multi-class classification)

Training configuration:

- Image size: 224 x 224
- Batch size: 32
- Epochs: 50
- Optimizer: Adam
- Loss function: Categorical Crossentropy

---

## Training and Evaluation

During training, the following metrics are monitored:

- Training accuracy
- Validation accuracy
- Training loss
- Validation loss

Performance curves are generated to analyze model behavior and detect overfitting or underfitting.

---

## Model Saving

The trained model is saved in HDF5 format:

mydata.h5

This allows the model to be reused for prediction without retraining.

---

## Prediction Pipeline

For prediction, each image is:

1. Resized to 224 x 224
2. Normalized
3. Converted to array format
4. Passed through the trained model

The Softmax output layer determines the predicted architectural class.

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- split-folders
- Jupyter Notebook / Google Colab

---

## Project Structure

├── Dataset/
├── train/
├── val/
├── mydata.h5
├── notebook.ipynb
└── README.md

---

## How to Run

1. Clone the repository:

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

2. Install dependencies:

pip install -r requirements.txt

3. Run the notebook:

jupyter notebook

Execute all cells to train and evaluate the model.

---

## Future Improvements

- Apply transfer learning (VGG16, ResNet, EfficientNet)
- Add data augmentation
- Perform hyperparameter tuning
- Deploy as a web application

---

## Authors

Assia Mouad  
Imane Ait Elmir  

Master ISI – Academic Year 2025/2026

---

## License

This project is developed for academic purposes.
