# microbiome
Microbiome CRC Prediction Model

This repository contains a machine learning project focused on predicting colorectal cancer (CRC) status using microbiome data. The primary objective is to leverage microbiome abundance data and metadata to classify patients into CRC or Healthy groups, while handling imbalanced datasets using SMOTE and training a highly accurate XGBoost model.

Table of Contents

Introduction

Dataset

Project Structure

Installation

Usage

Results

Acknowledgments

License

Introduction

Colorectal cancer is one of the most common cancers worldwide, and early detection can significantly improve treatment outcomes. The goal of this project is to develop a predictive model based on microbiome abundance data that can identify patients with CRC. The project utilizes the XGBoost classifier to build an accurate and robust model. Additionally, it uses SMOTE (Synthetic Minority Over-sampling Technique) to handle the inherent class imbalance in the dataset.

Dataset

The dataset used for this project was obtained from The Microbiome Atlas. The dataset contains microbiome abundance data along with metadata (e.g., age, BMI, gender) for each sample, with labeled information on the disease status (Healthy or CRC).

Features:

Age: Age of the participant.

BMI: Body Mass Index.

Gender: Categorical feature representing Male or Female.

Microorganism Abundances: Abundance values for various microorganisms present in each sample.

Target:

Disease_CRC: A binary variable representing whether the participant is healthy (0) or has CRC (1).

Project Structure

The project consists of the following files and directories:

├── data/                     # Directory for raw and processed data files
├── notebooks/                # Jupyter notebooks used for exploration and model training
├── README.md                 # Project overview and instructions


Features:

Data Preprocessing: The script handles missing values, normalizes features, and applies SMOTE to handle class imbalance.

Model Training: The model is trained using XGBoost with optimized hyperparameters.

Feature Importance: The model also provides feature importance scores to identify the most influential microbiome features for CRC prediction.

Results

Accuracy: The final model achieved an accuracy of 88% on the test set.

Recall for Disease_CRC: Recall for the CRC class improved significantly due to the use of SMOTE, leading to fewer false negatives.

Feature Importance: Important features include specific microorganism abundances, Age, and BMI.

Acknowledgments

I would like to thank The Microbiome Atlas for providing the microbiome abundance data used in this project. You can access the data from here
https://www.microbiomeatlas.org/downloads.php
