# Anti-Spoofing-Real-time-interview-analysis-system

A computer vision-based system designed to authenticate human presence during online interviews by detecting spoofing attempts using liveness detection, confidence scoring, and gaze tracking.

# Overview

This project focuses on building a real time pipeline that analyzes video input to verify and authenticate whether a candidate is real, physically present and attentive during an interview.

It aims to address common spoofing techniques such as:
- Static image attacks
- Pre-recorded video playback
- Lack of eye movement or engagement



# Key Features

- Face Detection using OpenCV  
-  Facial Landmark Detection using MediaPipe  
-  Gaze Tracking for attention monitoring  
-  Liveness Detection to distinguish real vs spoof inputs  
-  Confidence Scoring System for decision making  
-  Real-Time Processing Pipeline



# System Architecture
[ Video Input (Webcam) ]
            │
            ▼
[ Face Detection (OpenCV) ]
            │
            ▼
[ Facial Landmark Detection (MediaPipe) ]
            │
            ▼
[ Liveness Detection ]
 (Blink / Motion Analysis)
            │
            ▼
[ Gaze Tracking ]
 (Eye Movement Analysis)
            │
            ▼
[ Confidence Scoring System ]
 (Spoof Probability)
            │
            ▼
[ Final Output ]
 (Human / Spoof)



# Current Progress

- [x] Face Detection Module  
- [x] Landmark Detection using MediaPipe  
- [x] Basic Liveness Detection (Human Blinking-based)  
- [ ] Advanced Anti-Spoofing Model  
- [ ] UI Integration  
- [ ] Deployment  



# Performance (Prototype)

-  **Accuracy:** ~85% (based on initial testing)  
-  **Spoof Detection Improvement:** ~60–70% (simulated scenarios)  



#  Tech Stack

- **Languages:** Python  
- **Libraries:** OpenCV, MediaPipe, NumPy  
- **Tools:** VS Code, Git, GitHub  



# How It Works

1. Captures real-time video input from webcam  
2. Detects face and extracts eye landmarks  
3. Applies liveness detection (motion & eye blinks)  
4. Tracks eye gaze to analyze attention  
5. Generates a confidence score  
6. Verifies input as **Human or Spoof**




# Contributing

This is an ongoing project. Contributions, suggestions, and feedback are welcome.



# Contact

**Hrujuta Sonkusare**  
 Nagpur, India  
 hruju05@gmail.com  



## Note

This project is currently under development and will be continuously updated with new features and improvements.


