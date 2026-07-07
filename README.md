# Eye Blink Count 👁️

## 📌 Introduction

Eye Blink Count is a Python computer-vision project that detects and counts eye blinks from a video stream using facial landmarks. The system tracks eye key points frame-by-frame, calculates an eye aspect ratio proxy, and increments the blink counter when a blink pattern is detected.

---

## 🔄 Process / Flow

1. Open the input video stream (`Video.mp4`).
2. Detect face mesh landmarks for the face in each frame.
3. Extract key points around the left eye.
4. Compute vertical and horizontal eye distances.
5. Calculate the eye ratio and smooth it using recent frames.
6. Detect blink when ratio drops below threshold and debounce repeated counts.
7. Display live blink count and ratio plot on the output window.

---

## 🛠️ Technology Used

| Component | Technology |
|-----------|-----------|
| Language | Python |
| Computer Vision | OpenCV (`cv2`) |
| Face Landmark Detection | cvzone FaceMeshDetector |
| Visualization | cvzone LivePlot + OpenCV rendering |
| Numeric Operations | numpy |
| Backend Model Dependency | MediaPipe (via cvzone) |

---

## 🎓 Skills Gained

### Computer Vision Fundamentals

- ✅ Processing video frame-by-frame in real time
- ✅ Working with facial landmark coordinates for feature extraction
- ✅ Measuring geometric relationships to infer eye state

### Signal and Event Logic

- ✅ Smoothing noisy frame signals using a short rolling window
- ✅ Threshold-based event detection for blink identification
- ✅ Applying debounce/cooldown logic to avoid double counts

### Practical Python Implementation

- ✅ Building interactive visual output with overlays and plots
- ✅ Combining multiple CV utilities into one end-to-end pipeline
- ✅ Structuring an applied AI prototype with minimal dependencies

---

## 📂 Project Structure

```text
EyeBlink_Count-main/
├── blink.py                   # Main blink detection and counting script
└── README.md                  # Project documentation
```

---

## 📸 Demonstration

Video Demo:

[Video Demo Link](https://github.com/user-attachments/assets/c9ddf303-a5c4-4954-9dcf-eb2f71997507)

---

## ⚙️ Setup Instructions

### ✅ Prerequisites

- ✅ Python 3.8+
- ✅ Input video file named `Video.mp4` in the project root (or update the path in code)

### 📦 Installation

Install required packages:

```bash
pip install opencv-python numpy cvzone mediapipe
```

### ▶️ Run

Execute the script:

```bash
python blink.py
```
