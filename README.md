# Hand Gesture Controller (Virtual Mouse and Input System)

This project uses a webcam and computer vision (MediaPipe) to create a virtual input system that allows users to control the mouse, clicks, scrolling, system volume, and brightness using hand gestures.

## ✨ Features

  * **Virtual Mouse:** Move the cursor by moving your hand (`V_GEST`).
  * **Mouse Clicks:** Single-click, double-click, and right-click using distinct hand shapes.
  * **Drag & Drop:** Use a closed fist (`FIST`) to hold the left mouse button for dragging.
  * **Scrolling:** Scroll vertically and horizontally using the minor hand's pinch gesture (`PINCH_MINOR`).
  * **System Controls (Windows-only for Volume and Brightness):** Adjust system volume and screen brightness using the major hand's pinch gesture (`PINCH_MAJOR`).

## 💻 Prerequisites

Before running the script, ensure you have Python installed and a working webcam.

### Installation

Install the required Python libraries using `pip`:

```bash
pip install opencv-python mediapipe pyautogui screen-brightness-control
```

> ⚠️ **Windows Users:** For system volume control, you must also install `pycaw` and `comtypes`.

```bash
pip install pycaw comtypes
```

## 🚀 How to Run

1.  Save the provided code as a Python file (e.g., `gesture_controller.py`).
2.  Run the script from your terminal:

<!-- end list -->

```bash
python gesture_controller.py
```

3.  A window showing your webcam feed will open. The system will start tracking your hand movements and applying controls to your desktop.
4.  To exit, click on the video window and press the **ENTER** key.

## ✋ Gesture Guide

The system distinguishes between a **Major Hand** (Right Hand by default) for mouse control and a **Minor Hand** (Left Hand by default) for utility controls.

| Gesture | Hand | Action |
| :--- | :--- | :--- |
| **V-Sign** (`V_GEST`) | Major | **Move Mouse Cursor** |
| **Closed Fist** (`FIST`) | Major | **Left-Click Hold / Drag** |
| **Middle Finger Up** (`MID`) | Major | **Left-Click** (Single) |
| **Index Finger Up** (`INDEX`) | Major | **Right-Click** |
| **Index & Middle Together** (`TWO_FINGER_CLOSED`) | Major | **Double Left-Click** |
| **Index + Thumb Pinch** (`PINCH_MAJOR`) | Major | **System Volume (Y-axis) / Brightness (X-axis)** |
| **Index + Thumb Pinch** (`PINCH_MINOR`) | Minor | **Vertical & Horizontal Scroll** |

-----
