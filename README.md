## Hand Gesture Controlled Keyboard Input 

This project uses computer vision and hand gesture recognition to control keyboard inputs in real time. It is primarily designed for driving / racing games, where:

Closed fist (0 fingers) → Brake

Open hand (5 fingers) → Accelerator

The system detects hand landmarks using MediaPipe, processes gestures via OpenCV, and simulates keyboard key presses using Windows DirectInput (ctypes).

# Features

Real-time hand tracking using webcam

Accurate finger counting with MediaPipe Hands

Smooth key press & release handling

Works with most PC games and applications

Lightweight and fast execution

# Tech Stack

Python 3.8+

OpenCV

MediaPipe

ctypes (Windows API)

# Gesture Controls
Hand Gesture	Action	Key Pressed
Fist (0 fingers)	Brake	K
Open Hand (5 fingers)	Accelerator	M

You can change key mappings inside directkeys.py.


# Installation
Clone the Repository
git clone https://github.com/ShrishtiSingh26/hill_climbing.git
cd hill_climbing

# Install Dependencies
pip install opencv-python mediapipe


This project only works on Windows, because it uses SendInput via ctypes.

# How to Run
python main.py


Make sure your webcam is connected

Keep your hand clearly visible

Press Q to exit

# Key Configuration

Inside directkeys.py:

right_pressed = 0x4D  # M key
left_pressed  = 0x4B  # K key


You can change these scan codes to control different keys.

# How It Works

Webcam captures live video

MediaPipe detects hand landmarks

Finger count is calculated

Gesture is mapped to a keyboard key

Windows API simulates key press/release

# Use Cases

Racing & driving games

Accessibility tools

Gesture-based HCI systems

Computer vision learning projects

Human–Computer Interaction demos

# Limitations

Windows only

Requires good lighting

Designed for single hand detection

Uses webcam input (not optimized for mobile)

# License

This project is open-source and free to use for educational and personal projects.

# Contributing

Pull requests are welcome!
Feel free to improve gesture detection, add new gestures, or optimize performance.
