# Skin Disease Classification Pipeline

This repository contains resources for performing skin disease classification using machine learning techniques. It includes a testing framework based on extracted image features and pretrained models.

## Project Structure

* new\_images/
  Contains a collection of test images used for evaluating the classification model.

* extracted\_features/
  Includes `.npy` files storing:

  * Features extracted from the images in `new_images`
  * Image names corresponding to the features
  * Other intermediate or auxiliary feature arrays used for classification

* pca\_model.pkl
  A saved PCA model used for dimensionality reduction on image features.

* xgboost\_skin\_disease\_model.pkl
  A trained XGBoost classifier that predicts skin disease classes from the reduced features.

* combi\_classif.ipynb
  A Jupyter notebook that demonstrates the full pipeline: loading features, transforming them using PCA, and classifying them using the XGBoost model.

## How to Use

1. Ensure that Python and all necessary libraries are installed. Required packages include:

   * numpy
   * pandas
   * scikit-learn
   * xgboost
   * joblib

2. Open the `combi_classif.ipynb` notebook.

3. Follow the steps in the notebook to:

   * Load and verify the test image features
   * Apply PCA transformation
   * Run predictions using the XGBoost model
   * Display or store the classification results

## Purpose

This project provides a simple and modular pipeline to evaluate skin disease classification models on new data without retraining. It is particularly useful for testing inference performance and validating model accuracy on unseen samples.

## Note

This project assumes that image features have already been extracted using a consistent method that matches the training pipeline used for the saved models.
