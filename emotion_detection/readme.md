# Emotion Detector

This project is an emotion detector built using deep learning techniques. It can classify facial expressions into seven categories: angry, disgusted, fearful, happy, neutral, sad, and surprised.

## Dataset

The dataset used for training and testing the model is the [Emotion Detection FER](https://www.kaggle.com/datasets/ananthu017/emotion-detection-fer) dataset available on Kaggle. It contains grayscale images of faces labeled with their corresponding emotion.

## Model Architecture

The emotion detector model is built using a convolutional neural network (CNN) architecture implemented using TensorFlow and Keras. Here is an overview of the model architecture:

- Input layer: Grayscale image of size 48x48 pixels
- Convolutional layers: Multiple convolutional layers with batch normalization, max pooling, and dropout for feature extraction
- Fully connected layers: Dense layers for classification with batch normalization and dropout
- Output layer: Softmax activation to predict probabilities for each emotion class

## Training

The model is trained using the training subset of the dataset with data augmentation techniques such as random shifts and flips. The Adam optimizer with a learning rate of 0.001 is used, and the categorical cross-entropy loss function is optimized.

## Testing

After training, the model is tested on the validation subset of the dataset to evaluate its performance. Additionally, random samples from the test set are used to demonstrate the model's predictions.

## Usage

To use the emotion detector model, you can follow these steps:

1. Clone the repository: `git clone https://github.com/sv-medany/emotion-detector.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Run the model on your images or webcam feed.

## Example

Here's an example of how to use the model to detect emotions in an image:

```python
from emotion_detector import EmotionDetector

# Create an instance of the EmotionDetector
detector = EmotionDetector()

# Load an image
image_path = "path/to/your/image.jpg"

# Detect emotions
emotions = detector.detect_emotions(image_path)

print(emotions)
