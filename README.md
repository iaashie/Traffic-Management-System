# Intelligent Traffic Management System

An AI-powered traffic control system using real-time image processing and ultrasonic distance measurement to optimize traffic signal timings. This project is built using Raspberry Pi, YOLOv5, and OpenCV to ease urban congestion and improve traffic flow.

---

## Problem Statement

Traditional traffic lights use fixed signal durations, which are inefficient under dynamic traffic conditions. This system dynamically adjusts signal timing based on vehicle density measured using a camera and ultrasonic sensors.

---

## Objectives

- Capture real-time traffic images using a camera.
- Use YOLOv5 and OpenCV to detect and classify vehicles.
- Dynamically adjust green signal timing based on real-time vehicle count.

---

## Technologies & Tools

- Raspberry Pi (as control unit)
- 50MP Camera Module
- Python
- OpenCV
- YOLOv5 (Ultralytics)
- RPi.GPIO (for hardware control)

---

## Methodology

1. Setup: Install required libraries on Raspberry Pi.
2. Camera Calibration: Optimize for best traffic view.
3. Real-time Capture: Grab frames from the live feed.
4. Object Detection: Apply YOLOv5 to detect cars, bikes, etc.
5. Traffic Analysis: Count vehicles in each frame.
6. Signal Control: Adjust green light time accordingly.

---

## Algorithm Flow

1. Import libraries and load YOLOv5s model.
2. Read video stream or real-time feed.
3. For every 20th frame:
   - Detect vehicles
   - Count and classify
   - Calculate green signal duration:
     ```python
     green_time = BASE_GREEN_TIME + (vehicle_count * EXTRA_TIME_PER_VEHICLE)
     ```
4. Save frames with overlays.
5. Display results and release resources.

---

## Results

- Tested on real traffic footage from Karve Road, Pune.
- Accurate vehicle detection and dynamic signal timing.
- Improved traffic flow simulation compared to fixed-timing systems.

---

## Future Improvements

- Integrate with actual traffic lights and sensors.
- Train model with Indian traffic datasets for better accuracy.
- Add a user interface for real-time monitoring.
- Explore alternate ML models for faster processing.



