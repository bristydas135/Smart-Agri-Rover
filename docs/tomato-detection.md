# Tomato Detection

## Overview

Tomato ripeness detection is performed using the YOLOv5n object detection model.

## Dataset

The dataset contains 500 tomato images.

| Dataset | Images |
|---|---:|
| Training | 350 |
| Validation | 100 |
| Testing | 50 |
| Total | 500 |

## Classes

- Class 0 — Ripe tomato
- Class 1 — Unripe tomato

## Model

The project uses YOLOv5n for real-time tomato detection.

## Performance

| Metric | Result |
|---|---:|
| Precision | 85.18% |
| Recall | 76.24% |
| mAP@0.5 | 82.13% |
| mAP@0.95 | 44.19% |

## Deployment

The trained model was deployed on a Raspberry Pi 4 for real-time image processing using a USB camera.
