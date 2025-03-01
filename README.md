# INTELLOCK
INNOVATIVE DRUNK PREVENTATION PROJECT

## Overview
This project is a **real-time pupil detection system** that calculates the circumference of a person's pupils using **OpenCV** and **Dlib**. The system captures live video, detects facial landmarks, and measures the pupil circumference in millimeters. The data is stored in a CSV file for analysis.

## Features
- **Real-time pupil detection** using OpenCV and Dlib.
- **Accurate pupil circumference measurement** in millimeters.
- **Live visualization** of detected pupils and their measurements.
- **Data logging** in a CSV file for further analysis.
- **Automatic frame capturing** at a set frequency.

## System Requirements
- Python 3.x
- OpenCV (`cv2`)
- Dlib (`dlib`)
- NumPy (`numpy`)

## Installation
1. **Install dependencies**:
   ```bash
   pip install opencv-python dlib numpy
   ```
2. **Download Dlib’s facial landmark model**:  
   - Download `shape_predictor_68_face_landmarks.dat` from [Dlib Model](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2).
   - Extract it and place it in the same folder as the script.
     
3. **Run the program**:
   ```bash
   python pupil_detection.py
   ```

## How It Works
1. **Captures live video from the webcam**.
2. **Detects a face** and extracts **eye landmarks**.
3. **Calculates pupil diameter** and **converts it to circumference** using a fixed pixel-to-mm ratio.
4. **Displays the measurements in real-time**.
5. **Saves data periodically** in `pupil_data.csv`.

## CSV Data Format
The system logs the following information in `pupil_data.csv`:

| Left_Pupil_Circumference_mm | Right_Pupil_Circumference_mm |
|-----------------------------|-----------------------------|
| 1.45 mm                     | 1.67 mm                     |
| 2.23 mm                     | 2.45 mm                     |

## Customization
- **Adjust the frame capture frequency**:
  ```python
  write_frequency = 10  # Captures data every 10 frames
  ```
- **Change the pixel-to-mm ratio** (based on camera calibration):
  ```python
  pixels_per_mm = 15
  ```

## Potential Applications
- **Medical Analysis**: Detect neurological issues based on pupil size.
- **Driver Monitoring**: Measure pupil dilation in **drowsiness or impairment detection**.
- **Cognitive Research**: Track focus and cognitive load based on pupil dilation.





