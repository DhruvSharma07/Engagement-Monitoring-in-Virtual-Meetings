# Engagement Monitoring in Virtual Meetings
This project presents a real-time computer vision system designed to monitor participant engagement and detect spoofing during virtual meetings. Built using Python, OpenCV, and deep learning models, the system integrates Eye Aspect Ratio (EAR)-based drowsiness detection with YOLOv8n-based face anti-spoofing, providing a lightweight yet robust solution suitable for online education, corporate meetings, and remote assessments.

## Key Features
### Drowsiness Detection via EAR:
Tracks eye landmarks in real-time using dlib to compute Eye Aspect Ratio (EAR), flagging prolonged eye closure as a sign of fatigue or distraction.

### Face Anti-Spoofing with YOLOv8n:
Utilizes a custom-trained YOLOv8n model to detect and block spoofing attempts using printed photos or screen replays before behavioral analysis is performed.

### Parallel Multi-Stream Support:
Processes up to 4 live or recorded webcam streams simultaneously, displaying results in a 2×2 grid layout for centralized monitoring.

### Live Alerts and Engagement Scoring:
Flags drowsy or spoofed participants with on-screen alerts, and computes engagement scores based on real vs. inauthentic frame counts.

### Automated Reporting:
Generates session-wise engagement summaries and PDF reports, logging total frames, spoof instances, drowsiness incidents, and final attentiveness percentages.

## Tech Stack
- Languages: Python
- Libraries/Tools: OpenCV, dlib, YOLOv8 (Ultralytics), NumPy, Seaborn, Matplotlib, ReportLab
- Model Training: Custom dataset of real/spoof faces annotated in YOLO format; trained YOLOv8n model with 87% classification accuracy.
- Deployment: CPU-compatible and optimized for real-time performance without GPU dependency.

## Use Cases
- Remote Proctoring for Exams
- Corporate Virtual Interviews
- Driver Fatigue Monitoring
- Online Class Engagement Analysis

## Performance
- Spoof Detection Accuracy: 87%
- Real-Time Processing: ~50 FPS for 4 streams (CPU-based)
- Latency: <80ms per frame per stream on standard hardware

## Future Enhancements
- Add gaze and head pose estimation for deeper behavioral analysis.
- Integrate emotion detection to classify cognitive states.
- Support for cloud-based stream monitoring and dashboard analytics.
- Expand dataset with more diverse spoof and fatigue scenarios.
