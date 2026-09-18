# VisionGuard
### Modular Computer Vision Surveillance & Analytics Toolkit

[![Tests](https://img.shields.io/badge/pytest-31%20passed-brightgreen.svg)](#instructions-for-testing)
[![Python](https://img.shields.io/badge/python-3.10%20%7C%203.11%20%7C%203.12-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](#license)
[![OpenCV](https://img.shields.io/badge/OpenCV-Classical%20CV-orange.svg)](https://opencv.org/)

VisionGuard is a modular, fully offline computer-vision toolkit built for the **Computer Vision** flipped course evaluation. It provides four classical CV modules — face detection, motion tracking, object counting, and image enhancement — with an embedded SQLite persistence layer and automated analytical reporting.

Designed to be completely reproducible, self-contained, and executable from the terminal with zero external model downloads or cloud dependencies.

---

## Student Information
- **Author**: Himanshu Vatsha
- **Registration Number**: 24BAI10115
- **Course**: Computer Vision
- **Evaluation**: Build Your Own Project (Flipped Course Evaluation)
- **Platform**: VITyarthi
- **Date**: September 17, 2026

---

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [Technologies & Tools Used](#technologiestools-used)
- [Installation & Environment Setup](#installation--environment-setup)
- [Command-Line Usage Guide](#command-line-usage-guide)
  - [1. Face Detection](#1-face-detection)
  - [2. Object Counting](#2-object-counting)
  - [3. Motion Detection in Video](#3-motion-detection-in-video)
  - [4. Image Enhancement Filters](#4-image-enhancement-filters)
  - [5. Session History](#5-session-history)
  - [6. Audit Reporting & Analytics](#6-audit-reporting--analytics)
- [Instructions for Testing](#instructions-for-testing)
- [Design Decisions & Implementation Notes](#design-decisions--implementation-notes)
- [License](#license)

---

## Project Overview
Manual visual surveillance and manual counting of objects are time-consuming and error-prone. While modern deep learning has its merits, it often requires heavy GPU hardware, large pretrained weight files, complex CUDA setups, and cloud delays.

VisionGuard provides a clean CLI alternative using classical computer-vision algorithms implemented in OpenCV and Python:
1. **Zero External Downloads at Run Time**: Required Haar cascade XML and sample media are bundled directly.
2. **Deterministic & Reproducible**: Automated test suite with synthetic fixtures asserting exact mathematical counts.
3. **Pure Terminal Executability**: Clean sub-commands with sensible defaults and standard exit codes.
4. **Relational Audit Trail**: Built-in SQLite database tracking execution sessions and detections.

---

## Key Features
- **Face Detection (`faces`)**: Uses OpenCV's Haar Cascade classifier with histogram-equalization preprocessing.
- **Motion Detection (`motion`)**: Uses MOG2 background subtraction with shadow suppression.
- **Object Counting (`count`)**: Uses adaptive Gaussian thresholding and contour hierarchy analysis.
- **Image Enhancement (`enhance`)**: Filter registry providing edge detection, blur, sharpening, and thresholding.
- **Session Audit (`history`)**: Tabular CLI inspection of recent execution sessions.
- **Analytical Reporting (`report`)**: Exports session findings to JSON and CSV with comparison charts.

---

## Technologies & Tools Used
- **Language**: Python 3.10+
- **Computer Vision**: OpenCV (`opencv-python` >= 4.8.0)
- **Numerical Computing**: NumPy (`numpy` >= 1.24.0)
- **Data Visualization**: Matplotlib (`matplotlib` >= 3.7.0)
- **Database**: SQLite3
- **Testing**: Pytest (`pytest` >= 7.4.0)

---

## Installation & Environment Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/himanshuvatsha/visionguard.git](https://github.com/himanshuvatsha/visionguard.git)
cd visionguard


