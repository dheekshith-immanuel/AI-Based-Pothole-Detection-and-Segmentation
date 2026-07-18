# AI-Based Pothole Detection and Segmentation

## Project Overview

AI-Based Pothole Detection and Segmentation is a deep learning-based computer vision system designed to detect and segment potholes from road images and video streams in real time.

The project combines semantic segmentation and object detection techniques to provide pixel-level understanding of road conditions. It uses DeepLabV3 for scene-level segmentation and YOLOv8 segmentation for object-level detection, enabling accurate identification of potholes and other road elements.

The system processes raw video footage and converts it into meaningful visual information by highlighting damaged road areas, generating segmentation masks, and providing real-time performance analysis. This approach helps reduce manual road inspection efforts and supports efficient road safety monitoring.

---

## Key Features

- Real-time semantic segmentation using DeepLabV3-MobileNetV3.
- Pothole detection and segmentation using YOLOv8 segmentation models.
- Pixel-level identification of road damage areas.
- Real-time video and webcam input support.
- Automatic generation of annotated output videos.
- Live monitoring of FPS, inference latency, and processing performance.
- Visual enhancement using edge detection and image processing techniques.
- Screenshot capture during runtime.
- GPU acceleration with FP16 inference support.

---

## System Architecture

The system follows a three-stage computer vision pipeline:

### 1. Scene Segmentation
DeepLabV3-MobileNetV3 analyzes the complete scene and provides pixel-level classification of road environments.

### 2. Object Segmentation
YOLOv8 segmentation identifies individual objects and detects pothole regions using trained segmentation models.

### 3. Rendering and Visualization
The detected information is processed using OpenCV to generate visual overlays, segmentation masks, and real-time performance displays.

---

## Technologies Used

- Python
- PyTorch
- TorchVision
- DeepLabV3-MobileNetV3
- Ultralytics YOLOv8
- OpenCV
- NumPy
- PIL

---

## Performance Optimizations

- Lightweight DeepLabV3-MobileNetV3 backbone for faster inference.
- YOLOv8n-seg model for efficient object segmentation.
- GPU acceleration with CUDA and FP16 support.
- Optimized inference resolutions for real-time processing.
- Asynchronous inference pipeline to avoid blocking.
- Vectorized rendering for faster mask visualization.
- Frame optimization techniques for improved performance.

---

## Pothole Detection Module

The system can be extended for dedicated pothole detection by using a YOLOv8 segmentation model trained on pothole datasets.

The pothole detection module:
- Identifies pothole locations in road scenes.
- Generates segmentation masks around damaged areas.
- Highlights potholes for better visualization.
- Supports road safety analysis and maintenance planning.

A custom pothole-trained YOLOv8 segmentation model can be integrated by replacing the default segmentation model with the trained pothole model.

---

## Installation and Usage

Install the required dependencies:

```bash
pip install -r requirements.txt
