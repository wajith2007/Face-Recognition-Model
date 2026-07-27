# Face-Recognition-Model
This project develops a Facial Recognition System using Computer Vision, Deep Learning, and Machine Learning. OpenCV is used for image preprocessing, MobileNetV2 extracts facial features, and an SVM classifier recognizes individuals. The model predicts identities with high accuracy and evaluates performance using standard classification metrics.

# Facial Recognition System Using Computer Vision and Machine Learning

## Project Overview

This project implements a Facial Recognition System that identifies individuals using facial images from the **Olivetti Faces dataset**. The system combines Computer Vision and Machine Learning techniques to recognize different people based on their facial features. OpenCV is used for image preprocessing, Principal Component Analysis (PCA) is used for feature extraction through the Eigenfaces method, and a Support Vector Machine (SVM) classifier is trained to identify individuals. The model is evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.

## Dataset Details

The project uses the **Olivetti Faces dataset**, available in the Scikit-learn library.

* **Dataset:** Olivetti Faces
* **Source:** `sklearn.datasets.fetch_olivetti_faces()`
* **Total Images:** 400
* **Number of Persons:** 40
* **Images per Person:** 10
* **Image Size:** 64 × 64 pixels (Grayscale)

Each person has ten facial images captured under different expressions and lighting conditions.

## Preprocessing Steps

The following preprocessing techniques are applied before training:

1. Download the Olivetti Faces dataset from Scikit-learn.
2. Resize images (if required).
3. Normalize pixel values to improve model performance.
4. Convert images into NumPy arrays.
5. Flatten each image into a one-dimensional feature vector.
6. Split the dataset into training and testing sets.
7. Standardize the extracted features using StandardScaler.

## Feature Extraction

The project uses **Principal Component Analysis (PCA)**, also known as the **Eigenfaces** technique, for feature extraction.

* Reduces image dimensionality.
* Removes redundant information.
* Preserves the most important facial features.
* Improves training speed and classification performance.

## Facial Recognition Approach

The facial recognition system consists of the following stages:

* **Computer Vision (OpenCV):** Image preprocessing and normalization.
* **Feature Extraction (PCA/Eigenfaces):** Converts facial images into compact feature vectors.
* **Machine Learning (Support Vector Machine):** Classifies facial feature vectors into their corresponding identities.
* **Prediction:** Recognizes the person's identity from a test image.
* **Evaluation:** Measures model performance using accuracy, precision, recall, F1-score, and confusion matrix.

## Technologies Used

* Python
* OpenCV
* NumPy
* Scikit-learn
* PCA (Eigenfaces)
* Support Vector Machine (SVM)
* Matplotlib
* Joblib

## Project Workflow

1. Load the Olivetti Faces dataset.
2. Preprocess facial images.
3. Normalize image data.
4. Extract facial features using PCA (Eigenfaces).
5. Split the dataset into training and testing sets.
6. Train the SVM classifier.
7. Predict identities for unseen facial images.
8. Evaluate model performance.
9. Save the trained model for future predictions.

## Steps to Run the Project

1. Install the required Python libraries:

   ```bash
   pip install scikit-learn opencv-python matplotlib numpy joblib
   ```

2. Open the project in Jupyter Notebook.

3. Run the notebook cells in order:

   * Import libraries
   * Load the Olivetti Faces dataset
   * Preprocess images
   * Extract features using PCA
   * Train the SVM classifier
   * Test the model
   * Evaluate the results

4. Save the trained model using Joblib.

5. Use the trained model to predict the identity of new facial images.

## Output

The system provides:

* Predicted Person ID
* Prediction Confidence
* Training Accuracy
* Testing Accuracy
* Classification Report
* Confusion Matrix

## Future Enhancements

* Replace PCA with a pre-trained deep learning model such as FaceNet or MobileNetV2.
* Support real-time face recognition using a webcam.
* Improve recognition accuracy using larger face datasets.
* Deploy the model as a web or desktop application.

