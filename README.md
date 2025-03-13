# Music_Genre_Classification

This repository contains the code and report for Project: **Music Genre Classification**. The project focuses on classifying music into 10 different genres using various feature extraction methods and machine learning models.

## Overview

The project involves:
- **Dataset:** Music clips from 10 different genres with 100 audio samples per genre. Two CSV files provide parameters for 3-second and 30-second clips. Visual representations of the audio are created using mel-coefficients.
- **Data Preprocessing:** Audio files are trimmed to 30 seconds for uniformity and then segmented into 3-second clips to boost the dataset size.
- **Feature Extraction:** 
  - **Standard Extraction:** Spectral Rolloff, Spectral Bandwidth, Zero Crossing Rate, Chroma STFT, Mel Gibson Coefficients, Tempo, PLP, Harmony, and RMS. Mean and variance of these features are computed.
  - **Power Spectral Analysis:** Uses the Short-Time Fourier Transform (STFT) to obtain 519 Fourier transformations per clip. The power of each transformation is calculated and then separated into periodic and aperiodic components with the FOOOF library.
- **Machine Learning Models:** Various models were explored including:
  - **Basic Models:** Random Forest, XGBoost, LightGBM, Support Vector Machine, and different Neural Network architectures.
  - **Custom Models:** Ensemble methods that stack multiple model outputs with weighted averaging based on validation accuracy.

## Repository Contents

- `code.ipynb`: Jupyter Notebook containing the full code for data preprocessing, feature extraction, model training, and evaluation.
- `report.pdf` (and the LaTeX source files): The detailed project report.
- `README.md`: This file.

## Requirements

- **Python 3.x**
- **Jupyter Notebook**
- **Required Python Libraries:**  
  Install them using the command below 
  ```bash
  !pip install numpy pandas librosa scikit-learn xgboost lightgbm matplotlib tensorflow fooof
