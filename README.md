# Hand Gesture Detection Using OpenCV and MediaPipe

This project is a Python-based application that uses **OpenCV** and **MediaPipe** to detect hand gestures in real-time from a webcam feed. The application identifies specific gestures, displays the detected gesture on the video feed, and provides an interactive visual experience.

![Screenshot 2025-01-06 002144](https://github.com/user-attachments/assets/706b039b-0369-4442-b0d5-6598b0694ce4)

## Features
- **Real-Time Hand Tracking**: Detects hands and draws landmarks on the hand.
- **Gesture Recognition**: Identifies predefined gestures such as:
  - "I Love You"
  - "I Hate You"
  - "Hi"
  - "Bye"
  - "Kiss"
- **Interactive Visual Feedback**: Displays gesture names on the video feed.

## Prerequisites
Before running the program, ensure the following dependencies are installed:

- Python 3.7 or higher
- OpenCV
- MediaPipe

Install the required libraries with:
```bash
pip install opencv-python mediapipe
```

## How It Works

### Hand Detection
- **MediaPipe** detects hand landmarks in the video feed.
- The hand landmarks represent key points on the hand, such as fingertips and joints.

### Gesture Recognition
- The program uses the relative positions of hand landmarks to identify gestures.

#### Example gestures:
- **"I Love You"**: Thumb, index, and pinky fingers are up; middle and ring fingers are down.
- **"Hi"**: Thumb and index fingers are up; other fingers are down.

### Real-Time Feedback
- Detected gestures are displayed on the video feed using OpenCV.

## Usage

1. Clone the repository or copy the script.
2. Save the script as `gesture_detection.py`.
3. Run the script:
   ```bash
   python gesture_detection.py
   ```
4. The application will:
   - Open your webcam.
   - Display the video feed with hand landmarks and detected gestures.
   - Press `q` to exit the application.

## Code Overview

### Main Components

#### Gesture Detection
- The `detect_gesture()` function analyzes hand landmark positions to identify gestures.

#### Video Processing
- OpenCV captures frames from the webcam.
- The frames are processed to detect hands and display gesture names in real-time.

## Additional Notes
- Ensure proper lighting for better hand detection.
- Experiment with different gestures to explore the program's flexibility.
- Modify the `detect_gesture()` function to add custom gestures as needed.

## Troubleshooting
- If the webcam does not open, verify your camera permissions and device drivers.
- For better results, ensure the hand is fully visible to the webcam and avoid cluttered backgrounds.
