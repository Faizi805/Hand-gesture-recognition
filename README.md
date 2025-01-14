# Hand Gesture Recognition with OpenCV

## Overview

This project demonstrates real-time hand gesture recognition using OpenCV and NumPy. The application detects and interprets hand gestures captured through a webcam and displays the corresponding output. The program includes functionalities to filter and analyze hand movements within a defined Region of Interest (ROI).

## Features

- **Real-Time Detection**: Processes video input in real-time from the webcam.
- **Gesture Recognition**: Identifies up to five different gestures based on finger defects:
  - **ONE**: One finger detected.
  - **TWO**: Two fingers detected.
  - **THREE**: Three fingers detected.
  - **FOUR**: Four fingers detected.
  - **FIVE**: Five fingers detected.
- **Region of Interest**: Allows focusing on a specific area of the video feed for gesture recognition.
- **Contour and Convex Hull Detection**: Highlights hand contours and defects using convex hull analysis.

## Dependencies

The project requires the following libraries:

- OpenCV
- NumPy

Install the dependencies using pip:

```bash
pip install opencv-python numpy
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Faizi805/Hand-gesture-recognition.git
   ```


2. Run the script:
   ```bash
   python gesture_recognition.py
   ```

3. Adjust the ROI if necessary (optional, see future enhancements).

## Key Functionalities

### Image Filtering
The `imageFiltering()` function processes the frame to:
- Extract the ROI.
- Apply Gaussian Blur.
- Convert the image to HSV format.
- Threshold the image for specific color ranges.
- Detect contours and convex hulls for hand recognition.

### Gesture Recognition
The system uses the number of convexity defects in the hand contour to identify the gesture.

### Real-Time Display
Three windows are displayed:
- **Original Frame**: The webcam feed with ROI and gesture text.
- **Threshold Image**: The processed binary image for gesture detection.
- **Drawing**: The contour and convex hull overlay.

## Usage Instructions

- **Define ROI**: A rectangle is drawn around the predefined ROI in the video feed.
- **Gesture Detection**: Use gestures within the ROI to test the recognition system.
- **Exit**: Press the `Esc` key to quit the program.

## Code Highlights

- `imageFiltering(frame)`: Extracts and filters the ROI for gesture analysis.
- `cv2.findContours()`: Identifies the contours of the hand.
- `cv2.convexHull()`: Creates the convex hull for the hand contour.
- `cv2.convexityDefects()`: Identifies defects in the convex hull to count fingers.
- Gesture detection logic is based on the angle between finger defects.

## Future Enhancements

- **Dynamic ROI Adjustment**: Implement interactive ROI adjustment using mouse events.
- **Additional Gestures**: Extend recognition for more complex gestures.
- **Enhanced Filtering**: Use advanced algorithms to improve gesture accuracy under varying lighting conditions.
- **Integration with Applications**: Link gestures to specific actions, such as controlling slides or games.

---

This project is a starting point for more advanced gesture recognition systems. Feel free to fork and enhance it!

