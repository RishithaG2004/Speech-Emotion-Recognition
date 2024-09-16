# Speech Emotion Recognition

This project focuses on identifying emotions from speech using deep learning techniques. The dataset used is the **RAVDESS** (Ryerson Audio-Visual Database of Emotional Speech and Song), which consists of audio recordings of actors expressing various emotions.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Preprocessing](#preprocessing)
- [Model](#model)
- [Data Augmentation](#data-augmentation)
- [Conclusion](#conclusion)

## Project Overview
This project performs speech emotion recognition (SER) by extracting features such as Zero Crossing Rate (ZCR), MFCCs, Chroma, and Mel Spectrogram from audio files. These features are then fed into a Convolutional Neural Network (CNN) model for emotion classification.

## Dataset
The dataset used for this project is the **RAVDESS** dataset, which includes recordings of actors with different emotions such as:
- Neutral
- Happy
- Sad
- Angry
- Fear
- Disgust
- Surprise

## Installation
### Dependencies:
- Python 3.x
- TensorFlow
- Keras
- Librosa
- Matplotlib
- Seaborn
- Plotly
- Pandas
- Numpy
- Scikit-learn

## Preprocessing
Before feeding the audio data into the model, we performed the following preprocessing steps:
- Feature Extraction: Features such as ZCR, MFCC, Chroma, and Mel Spectrogram were extracted from the audio files using the librosa library.
- Data Augmentation: We applied noise injection, time stretching, pitch shifting, and shifting to increase the variety of training data.
- Normalization: StandardScaler was used to scale the features.

## Model
We built a CNN model for classification with the following architecture:
- 4 Conv1D layers with ReLU activation and MaxPooling
- Dropout layers to prevent overfitting
- A fully connected Dense layer
- Output layer with Softmax for multi-class classification
The model was trained using the Adam optimizer and categorical crossentropy as the loss function.

## Data Augmentation
To enhance the dataset and improve the model's performance, the following data augmentation techniques were applied:
- Adding white noise
- Time-stretching
- Pitch shifting
- Shifting the audio

## Conclusion
The model successfully classifies emotions from speech with good accuracy. Data augmentation played a crucial role in improving the model's performance by making the model more robust.
