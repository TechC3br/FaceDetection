FaceDetection
Introduction
This project aims to create a real-time system that detects face orientation (left, right, up, down) using OpenCV and MediaPipe. The system captures face images, trains a MobileNet convolutional neural network (CNN) for orientation prediction, and implements scroll and swipe operations using PyAutoGUI based on detected orientations.

Table of Contents
Features
Installation
Dataset Creation
Model Training Using MobileNet
Real-Time Face Orientation Prediction
Usage
Contributing
License
Features
Real-time face detection and orientation classification.
Efficient MobileNet architecture for rapid predictions.
Controls scrolling and swiping operations based on face orientation.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/TechC3br/FaceDetection.git
cd FaceDetection
Install required packages:

bash
Copy code
pip install opencv-python mediapipe tensorflow pyautogui numpy
Dataset Creation
To create the dataset for training the face orientation detection model, follow these steps:

Real-Time Video Capture: Use OpenCV’s cv2.VideoCapture() to capture live webcam feed.
Face Detection: Utilize MediaPipe’s Face Mesh model to detect facial landmarks and determine orientation.
Image Storage: Capture snapshots for each orientation and store them as labeled NumPy arrays.
Model Training Using MobileNet
Steps for Training:
Data Preprocessing: Resize and normalize the NumPy arrays of face images.
Model Architecture: Use MobileNet for its efficiency in image classification.
Training: Split the dataset into training and validation sets and train the model using TensorFlow/Keras.
Real-Time Face Orientation Prediction
After training the model, integrate it into a real-time system:

Load the Trained Model: Use TensorFlow/Keras to load the trained MobileNet model.
Real-Time Predictions: Process the webcam feed for face images and predict orientation.
Triggering PyAutoGUI Actions: Map predicted orientations to scrolling and swiping actions.
Usage
Run the main script to start the application. Ensure your webcam is active, and follow the instructions on-screen to capture your face in various orientations.

Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.
