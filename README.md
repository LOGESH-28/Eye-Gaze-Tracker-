# 🎯 Eye Gaze Tracker – Multi-User Real-Time Gaze Tracking System

An intelligent, multi-user gaze tracking system built in Python using OpenCV, MediaPipe, and Tkinter.  
Designed for environments where multiple users interact with a shared screen — ideal for research, accessibility, education, and human-computer interaction.

---

## 🧠 Overview

This project implements a complete eye-tracking pipeline:

- Face detection and unique identification (without saving biometric data).
- Prompting users to enter their names with a visual of their face.
- A gamified calibration interface using moving targets.
- Real-time gaze tracking with unique color-coded dots and names.
- Persistent user data across sessions using local storage.

All of this is presented through a clean, modern UI with dynamic styling and smooth UX.

---

## 🖼️ Features

- ✅ **Multi-user detection and registration**
- 🎮 **Animated, stress-free calibration system**
- 👁️ **Real-time gaze tracking using smoothed prediction**
- 🟢 **Unique colored dots with user names showing gaze focus**
- 🖥️ **Full-screen transparent overlay canvas**
- 💾 **Persistent user info (names, calibration models, color)**
- ⚡ **Live camera preview and FPS tracking**

---

## 📁 Project Structure

```text
├── main_app.py             # Entry point with dependency check and app boot
├── gaze_tracker_ui.py      # Modern Tkinter UI for user management, preview, status
├── gaze_tracker_logic.py   # Core tracking, face detection, calibration, model training
├── user_data.json          # Persistent data for user registry and trained models
└── README.md               # Project documentation


🛠️ Technologies Used
Python 3.10

OpenCV (cv2) – Video capture, image processing

MediaPipe – Face mesh landmark detection

Scikit-learn – Polynomial + RANSAC regression for gaze prediction

Tkinter – GUI framework with real-time updates and dialogs

Pillow – Image processing for face preview

JSON – Lightweight data persistence

Workflow:
Launch the system → Click “Start Tracking”

Each detected face is shown → User is prompted to enter a name

Once all users are named → Begin animated gamified calibration

After calibration → Colored, labeled dots track each person’s gaze in real-time


🧪 Calibration Details
9 randomized screen positions

Animated dot moves to encourage relaxed interaction

Captures multiple samples per user per dot

Uses regression models (Polynomial + RANSAC) to estimate gaze direction

Smooths gaze points using an exponential moving average


🔐 Privacy and Ethics
No facial images or biometric data are stored

Face data is used temporarily for registration only

Users are identified by name and session-local IDs
