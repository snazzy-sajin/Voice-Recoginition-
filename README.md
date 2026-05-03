# Voice Command Recognition using DSP and Machine Learning

## Overview

This project implements a speech-based command recognition system using Digital Signal Processing (DSP) and Machine Learning techniques. The system is capable of classifying short spoken commands such as *yes, no, up, down, on, off* from both pre-recorded audio and live microphone input.

The project is developed in Google Colab and demonstrates an end-to-end pipeline from raw audio acquisition to prediction using both classical and deep learning models.

---

## Objectives

* To process raw audio signals using DSP techniques
* To extract meaningful features using MFCC (Mel Frequency Cepstral Coefficients)
* To train and evaluate machine learning and deep learning models for classification
* To enable real-time voice command prediction in a browser environment

---

## System Architecture

Audio Input → Preprocessing → Feature Extraction → Model Inference → Output Prediction

---

## Methodology

### 1. Audio Preprocessing

* Resampling to a fixed sampling rate (16 kHz)
* Trimming and padding to maintain uniform signal length
* Conversion to mono channel
* Noise and silence handling

### 2. Feature Extraction

MFCC features are extracted from the audio signal, capturing both temporal and spectral characteristics essential for speech recognition.

### 3. Models Used

* **Random Forest Classifier**

  * Operates on statistical MFCC features (mean and standard deviation)
  * Provides a lightweight and interpretable baseline

* **Convolutional Neural Network (CNN)**

  * Operates on MFCC spectrogram-like inputs
  * Captures spatial patterns in audio features for higher accuracy
  <img width="1652" height="609" alt="image" src="https://github.com/user-attachments/assets/6d35a08c-6a9d-4694-8a73-2fcc07b1088b" />


### 4. Real-Time Prediction

Audio is captured from the browser microphone, converted from WebM format to WAV using FFmpeg, and then processed for prediction.

---

## Dataset

The project uses a subset of the Google Speech Commands dataset.

Classes used:

* yes
* no
* up
* down
* on
* off

---

## Technologies Used

* Python
* NumPy
* Librosa
* Scikit-learn
* TensorFlow / Keras
* Matplotlib
* Google Colab
* FFmpeg

---

## Installation and Setup

1. Open the notebook in Google Colab

2. Install dependencies:

```bash
pip install librosa soundfile
apt-get install -y ffmpeg
```

3. Run all cells sequentially:

   * Load dataset
   * Preprocess audio
   * Train models
   * Evaluate performance
   * Run live microphone prediction

---

## Results

* The Random Forest model provides fast and reliable baseline predictions
* The CNN model achieves higher accuracy due to its ability to learn complex feature patterns
* Real-time prediction works effectively with short voice commands under controlled noise conditions
<img width="814" height="672" alt="image" src="https://github.com/user-attachments/assets/bfa664d8-2c49-4a3b-86e4-38aa575dbea4" />

---

## Key Features

* End-to-end speech recognition pipeline
* Integration of DSP and machine learning concepts
* Support for both offline and real-time input
* Comparison between classical ML and deep learning approaches
* Browser-based microphone interaction in Colab

---

## Limitations

* Limited vocabulary (restricted command set)
* Performance depends on audio clarity and background noise
* Requires consistent sampling and preprocessing conditions

---

## Future Improvements

* Expand vocabulary and dataset size
* Implement noise reduction techniques
* Deploy as a web or mobile application
* Integrate with embedded systems (e.g., Arduino, IoT devices)
* Optimize models for real-time edge deployment

---

## Conclusion

This project demonstrates the practical integration of Digital Signal Processing and Machine Learning for speech recognition. It highlights how raw audio signals can be transformed into actionable insights using feature extraction and classification models, making it relevant for applications in automation, IoT, and human-computer interaction.

---

## Author

Sajin Praneeth S R
