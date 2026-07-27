# Face-Recognition-Model
This project develops a Facial Recognition System using Computer Vision, Deep Learning, and Machine Learning. OpenCV is used for image preprocessing, MobileNetV2 extracts facial features, and an SVM classifier recognizes individuals. The model predicts identities with high accuracy and evaluates performance using standard classification metrics.
# Facial Recognition System Using Machine Learning, Deep Learning, and Computer Vision

## Project Overview

This project implements a Facial Recognition System that identifies individuals from facial images using Computer Vision, Deep Learning, and Machine Learning techniques. The system uses OpenCV for image preprocessing, a pre-trained MobileNetV2 model for feature extraction, and a Support Vector Machine (SVM) classifier for facial recognition. The extracted facial features are used to train the classifier, which predicts the identity of a person from a given test image.

## Dataset Details

The project uses a custom face dataset organized into separate folders, where each folder represents a different person. Each folder contains multiple facial images of the corresponding individual captured under different poses and lighting conditions.

Example dataset structure:

```
dataset/
├── Person1/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
├── Person2/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
└── Person3/
    ├── img1.jpg
    └── ...
```

## Preprocessing Steps

The following preprocessing operations are performed before training the model:

* Load facial images from the dataset.
* Resize all images to the required input size.
* Normalize pixel values to improve model performance.
* Convert images into NumPy arrays.
* Split the dataset into training and testing sets.
* Extract deep feature vectors using the pre-trained MobileNetV2 model.

## Facial Recognition Approach

The facial recognition system combines Computer Vision, Deep Learning, and Machine Learning techniques:

* **OpenCV** is used for image loading, resizing, normalization, and preprocessing.
* **MobileNetV2 (Pre-trained Model)** is used as a deep feature extractor to generate high-level facial feature embeddings.
* **Support Vector Machine (SVM)** is trained on the extracted features to classify different individuals.
* The trained model predicts the identity of unknown faces and provides a confidence score for each prediction.

## Technologies Used

* Python
* OpenCV
* TensorFlow / Keras
* MobileNetV2 (Pre-trained Model)
* Scikit-learn
* NumPy
* Matplotlib
* Joblib

## Steps to Run the Project

1. Install the required Python libraries.
2. Organize the facial images into person-wise folders inside the `dataset` directory.
3. Open the project in Jupyter Notebook.
4. Run the preprocessing cells to load and prepare the images.
5. Extract facial features using the pre-trained MobileNetV2 model.
6. Train the SVM classifier using the extracted features.
7. Save the trained model and label encoder.
8. Run the prediction notebook or script to recognize faces from new images.
9. Evaluate the model using accuracy, precision, recall, F1-score, and confusion matrix.

## Output

The system displays:

* Predicted person's name
* Prediction confidence score
* Model accuracy
* Classification report
* Confusion matrix
