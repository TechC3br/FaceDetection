# FaceDetection

This project implements a real-time face orientation detection system using OpenCV and MediaPipe, powered by a MobileNet convolutional neural network (CNN). Based on the detected face orientation (left, right, up, down), the system triggers scrolling and swiping operations using PyAutoGUI.


## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Dataset Creation](#dataset-creation)
- [Model Training Using MobileNet](#model-training-using-mobilenet)
- [Real-Time Face Orientation Prediction](#real-time-face-orientation-prediction)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Real-time face detection and orientation classification** using MediaPipe's Face Mesh.
- **Efficient MobileNet CNN** architecture for rapid and accurate predictions.
- **Automated control** of scrolling and swiping based on face orientation with PyAutoGUI.

## Installation
To get started with this project, follow the steps below:

1. Clone the repository:
    ```bash
    git clone https://github.com/TechC3br/FaceDetection.git
    cd FaceDetection
    ```

2. Install the required dependencies:
    ```bash
    pip install opencv-python mediapipe tensorflow pyautogui numpy
    ```

## Dataset Creation
To train the face orientation model, create a custom dataset:

1. **Real-Time Video Capture**: Use OpenCV’s `cv2.VideoCapture()` to capture video from your webcam.
2. **Face Detection**: Detect facial landmarks using MediaPipe's Face Mesh.
3. **Capture and Label Images**: Capture images in different orientations (left, right, up, down) and store them as labeled NumPy arrays.

## Model Training Using MobileNet
The model is trained to predict face orientation based on the captured dataset.

### Steps:
1. **Data Preprocessing**: Resize and normalize the captured images.
2. **Model Architecture**: Use MobileNet for efficient and lightweight image classification.
3. **Training**: Split the dataset into training and validation sets, then train the model using TensorFlow/Keras.
4. **Saving the Model**: After training, save the trained MobileNet model for real-time predictions.

## Real-Time Face Orientation Prediction
Once the model is trained, integrate it into the real-time face orientation system:

1. **Load the Trained Model**: Use TensorFlow/Keras to load the trained MobileNet model.
2. **Predict Face Orientation**: Continuously capture and process webcam frames to predict face orientation.
3. **Trigger PyAutoGUI Actions**: Based on the predicted orientation, trigger corresponding PyAutoGUI actions (scrolling or swiping).

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Submit a pull request detailing your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
