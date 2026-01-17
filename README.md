# Facial Expression Recognition using CNN

This project detects human facial expressions in real-time using a webcam.

## Features
- Trained CNN (VGG-style) on grayscale facial images
- Real-time emotion prediction using OpenCV
- 7 emotion classes

## Model Architecture
- Custom VGG-style CNN
- Input: 48x48 grayscale face images
- Output: 7 emotion classes
- Activation: ELU + Softmax
- Optimizer: Adam

## Emotions Detected
Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

## Dataset Link
https://www.kaggle.com/datasets/msambare/fer2013

## Requirements
Install dependencies using:
pip install -r requirements.txt

## Training Details
- Dataset: FER2013 (28k+ images)
- Image Augmentation used
- Batch size: 32
- Epochs: 25
- Final Training Accuracy: ~43%

## How to Run
### 1. Train the model
python Clssification_little_vgg.py

### 2. Run real-time emotion detection
python Facial_Expression_Recog.py


## 📊 Model Accuracy

The trained VGG-style CNN achieved **~44% accuracy** on the FER2013 dataset.

Although this may seem low at first glance, it is actually a reasonable and expected performance for a custom CNN trained from scratch on FER2013.

### 🤔 Why accuracy is around 44%

FER2013 is a highly challenging dataset because:

- Images are very low resolution (48×48) and grayscale only  
- Facial expressions vary significantly across different people  
- Emotions like *Fear* and *Surprise* have very subtle differences  
- Dataset contains noise and some mislabelled samples  
- Class imbalance exists in multiple emotion categories  

### 📌 Benchmark Comparison

| Model Type | Typical Accuracy on FER2013 |
|------------|-----------------------------|
| Random Guess (7 classes) | ~14% |
| Basic CNN (trained from scratch) | 35–45% |
| Advanced models (ResNet / Transfer Learning) | 65–75% |

This project uses a **custom VGG-style CNN without transfer learning**, trained entirely on CPU. Therefore, achieving ~44% accuracy represents a solid baseline result.


## Notes
- Haarcascade is loaded using OpenCV built-in path
