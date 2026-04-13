# Face Recognition (2 Persons) – Real-Time AI

## Overview

This project implements a real-time face recognition system using a webcam. It identifies two predefined individuals and classifies all other faces as UNKNOWN. The system is optimized for GPU acceleration on NVIDIA RTX hardware. Project works only for two mainly because of hardware limitations.

## Key Features

* Real-time face detection and recognition
* Identification of selected individuals (2-person setup)
* Unknown face classification
* GPU acceleration using ONNX Runtime (CUDA)
* Lightweight and modular architecture

## Tech Stack

* Python 3.10+
* OpenCV
* InsightFace (ArcFace embeddings)
* ONNX Runtime GPU
* NumPy

## Project Structure

```
face2/
├── data/
│   ├── osoba1/
│   └── osoba2/
├── run.py
└── README.md
```

## Setup

```bash
python -m venv .venv
.\.venv\Scripts\activate
pip install --upgrade pip
pip install opencv-python numpy insightface onnxruntime-gpu
```

## Usage

1. Add images for each person:

```
data/osoba1/
data/osoba2/
```

2. Run the application:

```bash
python run.py
```

3. Press `Q` to exit.

## How It Works

* Captures frames from webcam
* Detects faces using a pre-trained model
* Generates embeddings (feature vectors)
* Compares embeddings with stored references
* Assigns identity or UNKNOWN based on similarity threshold

## Configuration

Recognition sensitivity can be adjusted in `run.py`:

```python
THRESH = 0.40
```

## Limitations

## * Performance depends on lighting conditions
## * Accuracy may decrease with occlusions or extreme angles

Project developed as part of a portfolio focused on AI and computer vision.
