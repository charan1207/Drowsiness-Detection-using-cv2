# Drowsiness-Detection-using-cv2

This Python application utilizes computer vision techniques to detect drowsiness in real-time using a webcam feed. It employs the dlib library for face detection and facial landmark localization, along with OpenCV for image processing.

## Key Features
# Face Detection: 
Utilizes dlib's frontal face detector to identify faces within the webcam feed.
# Facial Landmark Detection:
Employs dlib's shape predictor to locate facial landmarks such as eyes and mouth.
# Drowsiness Detection Algorithm:
Measures the average eye aspect ratio over a few consecutive frames to determine drowsiness. If the aspect ratio falls below a certain threshold for a prolonged period, it triggers an alarm indicating potential drowsiness.
# Real-time Feedback: Provides real-time visual feedback by drawing facial landmarks on the video feed and sounding an alarm when drowsiness is detected.

## Requirements
Python 3.x
OpenCV (cv2)
dlib
imutils
pygame

## Installation
1. Clone this repository to your local machine.
2. Install the required Python packages by running:
3. Download the pre-trained shape predictor model from the dlib website and place it in the root directory of the project.

# Algorithm:
# Facial Landmark Detection: 
The application uses the dlib library to detect facial landmarks in the webcam feed. Specifically, it identifies key points on the face, such as the corners of the eyes.
# Distance Calculation: 
By measuring the distance between specific pairs of facial landmarks (e.g., distance between eye corners), the application assesses whether the eyes are open or closed.
# Thresholding: 
A threshold value (thres) is set to determine the sensitivity of drowsiness detection. If the average distance between certain facial landmarks falls below this threshold for a sustained period, it indicates that the eyes are closed.
# Alert Mechanism: 
When drowsiness is detected (i.e., eyes closed for an extended duration), the system triggers an alarm to alert the person.

## Approach:
# Preparation: 
The necessary libraries such as OpenCV, dlib, imutils, and Pygame are imported. Additionally, a pre-trained shape predictor model (shape_predictor_68_face_landmarks.dat) is used for facial landmark detection.
# Webcam Feed: 
The application captures frames from the webcam in real-time.
# Facial Landmark Detection: 
Using dlib, the application detects facial landmarks in each frame. These landmarks include points around the eyes.
# Distance Calculation: 
By computing the distance between specific pairs of facial landmarks associated with the eyes, the application determines whether the eyes are open or closed.
# Drowsiness Detection: 
The average distance between relevant facial landmarks is compared to a threshold value (thres). If the average distance falls below this threshold for a certain duration, it indicates drowsiness.
# Alert Mechanism: 
When drowsiness is detected, an alarm sound is played using Pygame to alert the person.
# User Interface:
The application displays the webcam feed with facial landmark detection in real-time using OpenCV.

## Usage
1. Run the `drowsiness_detection.py` script.
2. A window will open showing the webcam feed with facial landmark detection.
3. If the system detects drowsiness (i.e., closed eyes for an extended period), it will trigger an alarm sound.

![image](https://github.com/charan1207/Drowsiness-Detection-using-cv2/assets/28255223/55f096fe-a40b-456b-a024-e8bb8796c7ec)


## Customization
- You can adjust the threshold value (`thres`) in the script to set the sensitivity of drowsiness detection.
- Customize the alarm sound by replacing the `alarm.wav` file with your preferred sound file.

## Acknowledgments
- This project utilizes the dlib library for facial landmark detection and OpenCV for image processing.
- Credits to imutils for providing convenient utilities for working with OpenCV.



