# Multi-Class Detection of Key Roles in Football

A deep learning project for automatically detecting and classifying key roles (players, referees, coaches, goalkeepers, and ball) in football match footage.

## Overview

This project implements state-of-the-art object detection models to identify and classify different roles in football matches. It uses **Faster R-CNN** and **RetinaNet** architectures for multi-class detection.

## Dataset

- **Format**: COCO (Common Objects in Context)
- **Classes**: 5 (Player, Referee, Coach, Goalkeeper, Ball)
- **Splits**: Training, Validation, and Test sets
- **Image Size**: 1000×1000 pixels (after resizing)

## Models

- **Faster R-CNN**: Two-stage detector with ResNet-50 + FPN backbone
- **RetinaNet**: Single-stage detector with focal loss for handling class imbalance

## Training

Both models are trained for 5 epochs with:
- Optimizer: Adam (lr=0.0001, weight_decay=0.0005)
- Batch Size: 1
- Learning Rate Scheduler: StepLR (step_size=3, gamma=0.1)

## Evaluation Metrics

- Validation Loss
- Average Detections per Image
- Average IoU (Intersection over Union)
- Class Accuracy

## Results

Both models successfully detect football roles with reasonable accuracy. RetinaNet's focal loss provides advantages for handling class imbalance inherent in the dataset.

## Author

Luigi Manieri (0001113044)
