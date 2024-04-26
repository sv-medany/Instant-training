
# Fire Detection using CNN

This project aims to detect the presence of fire in images using Convolutional Neural Networks (CNNs). It utilizes three popular pre-trained models: EfficientNetB0, VGG16, and ResNet50, to extract features from the images and classifies them into two categories: fire or non-fire.

## Dataset

The dataset used for training, validation, and testing consists of images containing fire and non-fire scenes. The dataset can be found at [Dataset for Fire Detection](https://www.kaggle.com/datasets/tharakan684/urecamain) on Kaggle.

## Model Architecture

Three pre-trained CNN models, EfficientNetB0, VGG16, and ResNet50, are used as base models. Classification layers are added on top of these base models to perform binary classification (fire or non-fire). Each model is compiled with the Adam optimizer and binary cross-entropy loss function.

## Training

The models are trained using the training subset of the dataset with data augmentation techniques such as random shifts, flips, shearing, and zooming. The training process is performed for 25 epochs.

## Evaluation

After training, the models are evaluated using the validation subset of the dataset to assess their performance. Finally, the best-performing model is selected based on accuracy metrics evaluated on the test set.

## Usage

To use the fire detection models, you can follow these steps:

1. Clone the repository: `git clone https://github.com/sv-medany/fire-detection.git`
2. Install the necessary dependencies: `pip install -r requirements.txt`
3. Run the models on your images or webcam feed to detect fire presence.

## Example

Here's an example of how to use the models to detect fire in an image:

```python
from fire_detector import FireDetector

# Create an instance of the FireDetector with the selected model (EfficientNetB0, VGG16, or ResNet50)
detector = FireDetector(model='EfficientNetB0')

# Load an image
image_path = "path/to/your/image.jpg"

# Detect fire presence
is_fire = detector.detect_fire(image_path)

if is_fire:
    print("Fire detected!")
else:
    print("No fire detected.")
