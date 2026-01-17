# Facial Expression Recognition using CNN

This project detects human facial expressions in real-time using a webcam.

## Features
- Trained CNN (VGG-style) on grayscale facial images
- Real-time emotion prediction using OpenCV
- 7 emotion classes

## Emotions Detected
Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

## Dataset Link
https://www.kaggle.com/datasets/msambare/fer2013

## Requirements
Install dependencies using:
pip install -r requirements.txt


## How to Run

### 1. Train the model
python Clssification_little_vgg.py


### 2. Run real-time emotion detection
python Facial_Expression_Recog.py


## Notes
- Haarcascade is loaded using OpenCV built-in path
