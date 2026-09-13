# ✋ Movement Tracking Using OpenCV

<h3>OUTPUT VIDEO</h3>




https://github.com/user-attachments/assets/476ee4fc-b80d-49fc-8d89-0cdbce1a7b10





<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-orange?style=for-the-badge" alt="MediaPipe">
  <img src="https://img.shields.io/badge/Real--Time-Tracking-purple?style=for-the-badge" alt="Real-Time Tracking">
  <img src="https://img.shields.io/badge/License-GPL--3.0-lightgrey?style=for-the-badge" alt="License">
</p>

<h3 align="center">
  Real-Time Hand Tracking and Movement Analysis Using Computer Vision
</h3>

<p align="center">
  A Python-based computer vision project that uses OpenCV and MediaPipe to detect hands, track hand landmarks, extract coordinates, and visualize movement through a live webcam feed.
</p>

---

## 📌 About the Project

**Movement Tracking** is a real-time computer vision application designed to detect and track human hand movements using a webcam.

The application captures video frames from the camera, processes them using OpenCV, and uses MediaPipe Hands to identify hand landmarks.

The detected landmarks are displayed directly on the live video stream. The application also provides landmark coordinate information and calculates the Frames Per Second (FPS) to monitor real-time processing performance.

This project demonstrates how computer vision can convert ordinary webcam footage into structured information that can be used for movement analysis and human-computer interaction.

---

## 🎯 Project Objectives

The primary objectives of this project are:

- ✋ Detect hands using a webcam.
- 📍 Track hand landmarks in real time.
- 🧭 Extract landmark coordinate information.
- 🟢 Highlight a selected hand landmark.
- 🎥 Process video frames continuously.
- ⚡ Display real-time FPS.
- 🧠 Demonstrate practical computer vision concepts.
- 🖥️ Build a foundation for gesture-based applications.

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🎥 Webcam Input | Captures live video from the computer's camera. |
| ✋ Hand Detection | Identifies hands present in the video frame. |
| 📍 Landmark Tracking | Detects and tracks important points on the hand. |
| 🧭 Coordinate Extraction | Accesses the coordinates of detected landmarks. |
| 🟢 Landmark Highlighting | Visually emphasizes a selected landmark. |
| ⚡ FPS Monitoring | Displays the current frame-processing rate. |
| 🔄 Real-Time Processing | Continuously processes incoming video frames. |
| 🖥️ Visual Feedback | Displays the processed camera feed with tracking information. |

---

## 🧠 Technologies Used

| Technology | Purpose |
|---|---|
| 🐍 Python | Main programming language. |
| 👁️ OpenCV | Webcam access, frame processing, drawing, and video display. |
| ✋ MediaPipe Hands | Hand detection and hand-landmark tracking. |
| 📦 pip | Python package installation and dependency management. |

---

## 🏗️ System Architecture

```text
                 ┌───────────────────────┐
                 │      USER HAND        │
                 └───────────┬───────────┘
                             │
                             ▼
                 ┌───────────────────────┐
                 │     WEBCAM INPUT      │
                 │   Live Video Frames   │
                 └───────────┬───────────┘
                             │
                             ▼
                 ┌───────────────────────┐
                 │        OpenCV         │
                 │ Frame Capture and     │
                 │ Image Processing      │
                 └───────────┬───────────┘
                             │
                             ▼
                 ┌───────────────────────┐
                 │    MediaPipe Hands    │
                 │ Hand Landmark         │
                 │ Detection             │
                 └───────────┬───────────┘
                             │
                             ▼
                 ┌───────────────────────┐
                 │   LANDMARK DATA       │
                 │ Coordinates and       │
                 │ Hand Structure        │
                 └───────────┬───────────┘
                             │
                  ┌──────────┴──────────┐
                  ▼                     ▼
       ┌───────────────────┐  ┌───────────────────┐
       │ Landmark          │  │ Coordinate        │
       │ Visualization     │  │ Extraction        │
       └─────────┬─────────┘  └─────────┬─────────┘
                 │                      │
                 └──────────┬───────────┘
                            ▼
                 ┌───────────────────────┐
                 │    FPS CALCULATION    │
                 └───────────┬───────────┘
                             │
                             ▼
                 ┌───────────────────────┐
                 │    LIVE VIDEO OUTPUT  │
                 │ Hand Tracking + FPS   │
                 └───────────────────────┘
```

---

## 🔄 Project Workflow

The application follows a continuous frame-processing pipeline:

```text
Start
  │
  ▼
Initialize Webcam
  │
  ▼
Capture Video Frame
  │
  ▼
Process Frame Using OpenCV
  │
  ▼
Detect Hand Landmarks Using MediaPipe
  │
  ▼
Are Hands Detected?
  │
  ├── No ──► Continue Capturing Frames
  │
  └── Yes
        │
        ▼
   Extract Landmark Data
        │
        ▼
   Access Coordinates
        │
        ▼
   Draw Hand Landmarks
        │
        ▼
   Highlight Selected Landmark
        │
        ▼
   Calculate FPS
        │
        ▼
   Display Live Video
        │
        ▼
   Repeat
```

---

## 🔍 How the Project Works

### 1. Webcam Input

The webcam acts as the primary input device.

OpenCV continuously captures frames from the computer's camera. Each frame represents a single image from the live video stream.

```text
Webcam
   ↓
Live Video Frames
   ↓
OpenCV
```

---

### 2. Frame Processing Using OpenCV

OpenCV provides the computer vision functionality required to:

- Access the webcam.
- Read video frames.
- Process image data.
- Convert frames into the required format.
- Draw landmarks and graphical elements.
- Display the processed video stream.

OpenCV acts as the connection between the physical camera and the computer vision pipeline.

---

### 3. Hand Landmark Detection Using MediaPipe

MediaPipe Hands processes the video frames to identify hand landmarks.

A detected hand is represented using a structured set of landmark points. These points provide information about the positions of important parts of the hand, including the wrist and finger joints.

The detected landmark data can be used for:

- Hand visualization.
- Coordinate extraction.
- Finger tracking.
- Gesture recognition.
- Human-computer interaction.

---

### 4. Landmark Visualization

Once the hand landmarks are detected, the application draws them over the original video frame.

This allows the user to observe how the detected landmarks follow hand movement in real time.

The project also highlights a selected landmark using a filled circle.

---

### 5. Landmark Coordinates

The application accesses the coordinate information returned by MediaPipe.

These coordinates provide a numerical representation of the detected hand.

Conceptually:

```text
Real Hand
    ↓
Camera Image
    ↓
MediaPipe Detection
    ↓
Hand Landmark Data
    ↓
Coordinate Information
    ↓
Computer-Readable Hand Representation
```

The coordinate data can later be used to develop gesture recognition, movement analysis, and interactive control systems.

---

### 6. FPS Monitoring

The application calculates and displays the Frames Per Second, or FPS.

FPS represents the number of video frames processed per second.

```text
Higher FPS  → Smoother visual tracking
Lower FPS   → Slower visual response
```

FPS provides a basic indication of the application's real-time processing performance.

---

## 📁 Project Structure

The repository contains the following core files and folders:

```text
MOVEMENT-TRACKING/
│
├── 📂 Data Sources and Artifacts/
│   └── Project-related data and supporting artifacts
│
├── 🐍 Hand Tracking from Media .py
│   └── Hand-tracking implementation using Python
│
├── 🐍 app.py
│   └── Main application entry point
│
├── 📄 requirements.txt
│   └── Python dependency list
│
├── 📄 .gitignore
│   └── Files excluded from version control
│
├── 📄 LICENSE
│   └── Project licensing information
│
└── 📄 README.md
    └── Project documentation
```

> **Note:** The repository contains both `app.py` and `Hand Tracking from Media .py`. Use the appropriate script for the implementation you want to execute.

---

## ⚙️ Installation and Setup

### Prerequisites

Before running the project, make sure you have:

- Python 3.x installed.
- A working webcam.
- pip installed.
- A computer capable of running real-time video processing.
- Required Python libraries.

---

### Step 1: Clone the Repository

```bash
git clone https://github.com/keshavkapill/MOVEMENT-TRACKING.git
```

Navigate to the project directory:

```bash
cd MOVEMENT-TRACKING
```

---

### Step 2: Create a Virtual Environment

Creating a virtual environment is recommended to keep project dependencies isolated.

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

Activate the environment on macOS or Linux:

```bash
source venv/bin/activate
```

---

### Step 3: Install Dependencies

Install the packages listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

The project primarily uses:

- OpenCV
- MediaPipe

---

## ▶️ Running the Project

Run the main application:

```bash
python app.py
```

If you want to execute the other hand-tracking script, use its actual filename:

```bash
python "Hand Tracking from Media .py"
```

> Make sure the selected script contains the intended executable application logic.

---

## 🖥️ Expected Output

When the application is running, it should provide a live camera window containing hand-tracking information.

Expected functionality includes:

### ✋ Hand Detection

The application identifies hands visible in the camera feed.

### 📍 Landmark Visualization

Detected hand landmarks are drawn over the video frame.

### 🧭 Landmark Coordinates

The application accesses coordinate data associated with detected landmarks.

### 🟢 Selected Landmark Highlighting

A selected landmark is emphasized using a visual marker.

### ⚡ FPS Display

The live video output displays the current frame-processing rate.

---

## 🧪 Functional Breakdown

```text
INPUT
  └── Webcam Video

PROCESSING
  ├── OpenCV
  │   ├── Capture Frame
  │   ├── Process Frame
  │   └── Display Frame
  │
  └── MediaPipe Hands
      ├── Detect Hand
      └── Locate Landmarks

OUTPUT
  ├── Landmark Visualization
  ├── Landmark Coordinates
  ├── Highlighted Landmark
  └── FPS Information
```

---

## 🌐 Potential Applications

The hand-tracking foundation developed in this project can be extended to several practical applications.

### 🕹️ Gesture-Controlled Systems

Hand landmarks can be used to recognize gestures and control software applications.

### 🎮 Gaming

Hand movements can serve as input for interactive games.

### 🖥️ Human-Computer Interaction

The system can support touchless interaction between users and computers.

### 🥽 Virtual and Augmented Reality

Hand tracking can provide a foundation for natural interaction in immersive environments.

### ♿ Accessibility Interfaces

Gesture-based controls may provide alternative interaction methods for users.

### 📊 Movement Analysis

Landmark coordinates can be analyzed to study hand movement patterns and trajectories.

---

## 🚀 Future Development Roadmap

The current hand-tracking system can be expanded into a more advanced gesture-recognition platform.

```text
Hand Landmark Tracking
          │
          ▼
     Finger Detection
          │
          ▼
   Gesture Recognition
          │
          ▼
  Gesture Classification
          │
          ▼
    Command Generation
          │
          ▼
   Real-World Interaction
```

### Planned Improvements

- ☝️ Finger-count detection.
- 👍 Custom gesture recognition.
- 🖱️ Virtual mouse control.
- ✍️ Air drawing.
- ⌨️ Gesture-based keyboard interaction.
- 🎵 Gesture-controlled media player.
- 🎮 Gesture-based gaming.
- 📍 Landmark coordinate recording.
- 📈 Movement trajectory analysis.
- 🤖 Gesture-triggered automation.
- ⚡ Improved tracking performance.

---

## ⚠️ Troubleshooting

### Camera Does Not Open

Check the following:

- Ensure the webcam is connected.
- Verify that camera permissions are enabled.
- Close other applications using the webcam.
- Check whether the correct camera device is selected.

### Dependencies Fail to Install

Verify your Python installation:

```bash
python --version
```

Then try installing the dependencies again:

```bash
pip install -r requirements.txt
```

### Low FPS

Real-time performance may be affected by:

- CPU performance.
- Camera resolution.
- Frame-processing workload.
- Number of detected hands.
- Background complexity.
- Other applications running simultaneously.

Try reducing the camera resolution or closing unnecessary applications.

### Hand Landmarks Are Not Detected Properly

Try the following:

- Improve lighting conditions.
- Keep your hand within the camera frame.
- Avoid excessive motion blur.
- Ensure that the camera lens is clean.
- Maintain a suitable distance from the camera.

---

## 🧠 Concepts Demonstrated

This project provides practical exposure to:

### Computer Vision

- Real-time video capture.
- Image and frame processing.
- Hand landmark detection.
- Visual tracking.
- Computer vision pipelines.

### Python Programming

- Functions.
- Loops.
- Conditional statements.
- Coordinate handling.
- External library integration.
- Real-time application development.

### Media Processing

- Frame-by-frame analysis.
- Live video processing.
- Visual output generation.
- FPS calculation.

### Human-Computer Interaction

- Hand movement tracking.
- Vision-based interaction.
- Gesture-based control foundations.

---

## 💡 Why This Project Is Useful

This project demonstrates how a standard webcam can be transformed into an interactive computer vision input device.

Instead of treating camera footage as ordinary video, the application extracts structured information from the visual scene.

```text
Camera Feed
     ↓
Visual Information
     ↓
Hand Detection
     ↓
Landmark Data
     ↓
Coordinate Information
     ↓
Computer Interaction
```

This makes the project a useful foundation for learning computer vision and developing more advanced hand-tracking and gesture-based applications.

---

## 👨‍💻 Developer

**Keshav Kapil**

Computer Science student interested in:

- Software Development
- Data Analytics
- Cloud Computing
- Computer Vision
- Full-Stack Development

---

## 🤝 Connect With Me

<p align="left">
  <a href="https://github.com/keshavkapill">
    <img src="https://img.shields.io/badge/GitHub-Keshav%20Kapil-black?style=for-the-badge&logo=github" alt="GitHub">
  </a>
  <a href="https://www.linkedin.com/in/keshavkapil15">
    <img src="https://img.shields.io/badge/LinkedIn-Keshav%20Kapil-blue?style=for-the-badge&logo=linkedin" alt="LinkedIn">
  </a>
</p>

---

## 📄 License

This project is distributed under the **GNU General Public License v3.0**.

Refer to the `LICENSE` file for complete licensing details.

---

<p align="center">
  ✋ Track • Detect • Visualize • Interact
</p>

<p align="center">
  ⭐ Thanks for visiting the project!
</p>
