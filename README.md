# Smart-Agri-Rover

## Agricultural Rover for Vegetable Harvesting and Soil Analysis

A multifunctional agricultural rover designed for vegetable harvesting and soil analysis, integrating robotics, computer vision, YOLOv5-based tomato ripeness detection, a 6-DOF robotic arm, and NPK soil sensing for precision agriculture.

## Overview

Agricultural labor shortages, crop monitoring challenges, and the need for efficient soil management have increased the demand for smart agricultural technologies. This project presents a multifunctional agricultural rover designed to support vegetable harvesting, tomato ripeness detection, soil analysis, and field monitoring.

The system integrates a Raspberry Pi 4, Arduino controllers, computer vision, a YOLOv5 object detection model, a 6-DOF robotic arm, and an NPK soil sensor.

## Key Features

* 🍅 Tomato ripeness detection using YOLOv5n
* 🦾 6-DOF robotic arm for vegetable harvesting
* 🌱 NPK-based soil nutrient analysis
* 📷 Camera-based crop monitoring
* 🤖 Robotic harvesting mechanism
* 📡 Wi-Fi-based rover control
* 🍃 Ripe and unripe tomato classification
* 🧠 Real-time image processing using Raspberry Pi 4

## AI-Based Tomato Detection

The tomato detection system uses YOLOv5n for real-time object detection.

### Dataset

* Total images: 500
* Training images: 350
* Validation images: 100
* Test images: 50
* Classes:

  * 0 — Ripe tomato
  * 1 — Unripe tomato

### Model Performance

| Metric    | Result |
| --------- | -----: |
| Precision | 85.18% |
| Recall    | 76.24% |
| mAP@0.5   | 82.13% |
| mAP@0.95  | 44.19% |

The trained model was deployed on a Raspberry Pi 4 for real-time image processing using a USB camera.

## Robotic Harvesting

The rover uses a 6-degree-of-freedom robotic arm equipped with six MG996R servo motors. A two-finger V-shaped claw with blades is used to grasp and cut the tomato branch during harvesting.

The harvesting process consists of:

1. Tomato detection
2. Ripeness classification
3. Rover positioning
4. Robotic arm positioning
5. Tomato grasping
6. Branch cutting
7. Tomato collection

## Soil Analysis

The rover incorporates an NPK soil sensor to measure:

* Nitrogen (N)
* Phosphorus (P)
* Potassium (K)

An RS-485 communication module is used to transmit sensor data to an Arduino UNO for processing.

## Hardware

Major hardware components include:

* Raspberry Pi 4
* Arduino Mega
* Arduino UNO
* USB camera
* DC motors
* Monster motor driver
* 12V battery
* Buck converter
* NPK soil sensor
* RS-485 module
* Six MG996R servo motors
* 6-DOF robotic arm
* Two-finger harvesting claw

## System Architecture

The rover combines several subsystems:

```text
                    SMART AGRI ROVER
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
    Rover Control     Computer Vision   Soil Analysis
          │                │                │
          │             YOLOv5n          NPK Sensor
          │                │                │
          │       Tomato Detection       RS-485
          │                │                │
          └────────────┬───┴────────────────┘
                       │
                       ▼
                Robotic Harvesting
                       │
                       ▼
                 6-DOF Robotic Arm
```

## Experimental Results

The developed prototype demonstrated the integration of tomato detection, robotic harvesting, and soil nutrient analysis.

Example NPK sensor measurements were compared with a commercial Aqualink system:

| Nutrient   | NPK Sensor |  Aqualink |
| ---------- | ---------: | --------: |
| Nitrogen   |   74 mg/kg |  54 mg/kg |
| Phosphorus |   68 mg/kg |  73 mg/kg |
| Potassium  |  181 mg/kg | 172 mg/kg |

## Limitations

The current prototype faces challenges related to:

* Operation in unstructured agricultural environments
* Muddy and wet soil conditions
* Robust crop detection and classification
* Human–automation interaction

## Future Work

Future development may focus on:

* Improved object detection and classification
* Multimodal sensing
* RGB, multispectral, and LiDAR integration
* Improved edge/on-device AI processing
* Autonomous navigation
* Autonomous path planning
* Advanced AI and robotics integration
* Agricultural data analytics
* Decision-support systems

> Note: Autonomous navigation and path planning are considered future improvements; the current prototype uses remote/Wi-Fi control.

## Publication

**Designing and development of agricultural rovers for vegetable harvesting and soil analysis**

Published in *PLOS ONE*, 2024.

DOI: 10.1371/journal.pone.0304657

## Citation

If you use this project or its research, please cite the associated publication.

## License

This repository is licensed under the MIT License. See the `LICENSE` file for details.

