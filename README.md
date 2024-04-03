# Driver Drowsiness Detection

This project aims to detect drowsiness in drivers using computer vision techniques. It utilizes facial landmarks and eye aspect ratios to determine if the driver's eyes are closed for an extended period, indicating drowsiness.

## How it Works

- The project detects faces in the video stream using the dlib library and its pre-trained face detector.
- It then extracts facial landmarks to locate the eyes and calculates the eye aspect ratio (EAR) to determine if the eyes are closed.
- If the EAR falls below a predefined threshold for a certain number of consecutive frames, an alarm is triggered to alert the driver.
- The project continuously monitors the video stream from the webcam and updates the user interface in real-time to indicate drowsiness detection.

## Prerequisites

- Python 3.x
- OpenCV (cv2)
- NumPy
- imutils
- dlib
- playsound

## Getting Started

1. Clone the repository and headout to project directory and run `pip install -r requirements.txt`.
2. Download the pre-trained shape predictor file (`shape_predictor_68_face_landmarks.dat`) from the dlib website.
3. Ensure you have an alarm sound file (`alarm.wav`) placed in the project directory.
4. Run the `drowsiness.py` script.
5. Press 'q' to exit the video stream.

## Project Structure

- `drowsiness.py`: Main Python script containing the drowsiness detection logic.
- `alarm.wav`: Alarm sound file played when drowsiness is detected.

## Customization

- You can adjust parameters like `EYE_AR_THRESH` and `EYE_AR_CONSEC_FRAMES` in the script to fine-tune the drowsiness detection sensitivity.
- Modify the alarm sound file (`alarm.wav`) to your preference.

For any issues or suggestions, feel free to open an issue.
