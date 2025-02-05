# Color_Based_Fire_Detection

Overview

This project implements a real-time fire detection system using OpenCV and color-based segmentation. It captures video from the webcam, detects red flames using HSV color thresholding, and triggers an alarm sound when fire is detected.

Features

Real-time fire detection using color-based segmentation.

Plays an alarm sound when fire is detected.

Uses Matplotlib for frame display instead of OpenCV's imshow().

Includes a cooldown mechanism to avoid repeated alerts.

Requirements

Ensure you have the following dependencies installed before running the script:

pip install opencv-python numpy matplotlib playsound

File Structure

📂 Fire Detection Project
├── fire_detection.py  # Main script
├── mixkit-classic-alarm-995.wav  # Alarm sound file
└── README.md  # Project documentation

How It Works

Captures video from the webcam.

Converts each frame to the HSV color space.

Applies a color threshold to detect red flames.

Identifies fire regions using contour detection.

Triggers an alarm sound (.wav file) when fire is detected.

Implements a cooldown mechanism to avoid repeated alerts.

Displays the processed frame using Matplotlib.

Usage

Run the script using:

python fire_detection.py

Troubleshooting

🔴 File Not Found Error for Alarm Sound

If you see FileNotFoundError for the alarm sound, ensure that:

The .wav file exists in the correct directory.

The file path is properly formatted. Use either:

alert_sound = r"C:\Path\To\mixkit-classic-alarm-995.wav"

or

alert_sound = "C:/Path/To/mixkit-classic-alarm-995.wav"

🔴 No Webcam Detected

If the webcam is not detected, ensure that:

Your camera is connected and not being used by another application.

Try changing the video source:

cap = cv2.VideoCapture(1)  # Try 1 instead of 0

License

This project is open-source and free to use.

Author

Developed by Muthusingam N
