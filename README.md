# Jump Height Estimation using MediaPipe Pose Detection

A python-based system that analyzes video to estimate vertical jump height by tracking body land marks using MediaPipe.

## Table of contents
-[Features]
-[How it works]
-[Installation]
-[Usage]
-[Example Results]
-[Next Steps]

## Features
Process video files to analyze jumps
uses MediaPipe pose for accurate body landmark detection
Tracks hip movement to calculate vertical displacement
Generates visualization of movement over time
Computes normalized jump height from pixel coordinates

## How it works
1.**Pose detection**
Uses MeiaPipe to identify 33 body landmarks
Focuses on left hip (Landmark 23)

2.**Movement Tracking**
Records  vertical (y-axis) position each frame
Normalizes coordinates between 0-1

3.**Height Calculation**
'''Python
min_y = min(hip_y_positions)
max_y = max(hip_y_positions)
jump_height_norm = max_y - min_y

4.**Visualization**
Plots hip position vs frame number
Inverts y-axis for intuitive display

## Installation
The notebook includes all installation commands

## Usage
Video 1.mp4

example:
In Colab notebook:
uploaded = files.upload()
video_path = list(uploaded.keys())[0]

## Example Results
Normalized Jump Height (Hip): 0.2191

## Next Steps
Planned Improvements
1.**Add real-world height calibration**
2.**Implement webcam live processing**
3.**Track multiple landmarks (shoulders, knees)**
4.**Create web interface version**

