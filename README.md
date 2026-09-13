<div align="center">

✋ Hand Tracking Using OpenCV

Real-Time Computer Vision • MediaPipe • Webcam Tracking

<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-FF6F00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Real--Time-Webcam%20Processing-00A98F?style=for-the-badge"/>
</p>

A real-time hand-tracking application that uses a webcam, OpenCV, and MediaPipe to detect hands, visualize hand landmarks, display landmark coordinates, and monitor processing performance.

</div>

🎥 Project Demo

The project includes a demonstration of the real-time hand-tracking application:

https://github.com/keshavkapill/Hand-Tracking-Using-Opencv/assets/101493756/e0d7fae9-4a16-4639-b5fe-04d5c7f6ce38

📌 About the Project

Hand Tracking Using OpenCV is a Python-based computer vision project that performs real-time hand detection and landmark tracking through a webcam.

The application continuously captures frames from the default camera, processes those frames using OpenCV, and passes the visual information to MediaPipe Hands for hand landmark detection.

For each detected hand, the application visualizes the detected landmarks on the live camera feed. It also accesses the landmark coordinates and highlights landmark index 0 with a filled circle.

In addition, the application calculates and displays the Frames Per Second (FPS), providing a simple indication of how efficiently the application is processing the live video stream.

The project demonstrates the complete flow from:

Camera Input
     ↓
Frame Processing
     ↓
Hand Detection
     ↓
Landmark Detection
     ↓
Coordinate Extraction
     ↓
Visualization
     ↓
FPS Measurement

🎯 Project Objectives

The main objectives of this project are:

✋ Detect hands from a live webcam stream

📍 Track the landmarks associated with detected hands

🧭 Access and print landmark coordinates

🟢 Highlight landmark index 0

🎥 Process video frames continuously in real time

⚡ Measure and display FPS

🧠 Demonstrate practical computer vision concepts using Python

🧩 Core Elements of the Project

1. 🎥 Webcam Input

The webcam acts as the primary input source.

The application continuously captures frames from the computer's default camera and processes them one by one.

Webcam
  ↓
Live Video Frames
  ↓
OpenCV Processing

2. 👁️ OpenCV

OpenCV is used as the computer vision layer of the project.

It provides the functionality required to:

Access the webcam

Read video frames

Process frames

Draw graphical elements

Display the processed video stream

Support real-time FPS visualization

OpenCV therefore acts as the bridge between the physical camera and the visual output shown to the user.

3. ✋ MediaPipe Hands

MediaPipe Hands performs the hand landmark detection portion of the application.

The visual frame is processed to identify a hand and determine the positions of its landmarks.

The resulting landmark data can then be used for:

Visualization

Coordinate extraction

Gesture analysis

Interaction systems

Future gesture-recognition functionality

4. 📍 Hand Landmarks

The project works with the landmark information returned by MediaPipe.

The landmarks provide structured coordinate data representing important points on a detected hand.

Conceptually:

                    Hand
                     │
       ┌─────────────┴─────────────┐
       │                           │
  Landmark Data              Hand Connections
       │                           │
       └─────────────┬─────────────┘
                     │
                     ▼
              Visual Output

The project specifically highlights landmark 0 using a filled circle.

5. 📊 Landmark Coordinates

For every detected hand, the program accesses the coordinates associated with the detected landmarks.

These coordinates are printed by the application and form the numerical representation behind the visual tracking system.

The basic concept is:

Real Hand
   ↓
Camera Image
   ↓
MediaPipe Detection
   ↓
Landmark Coordinates
   ↓
Computer-readable Hand Representation

6. ⚡ FPS Monitoring

The application calculates the frame rate and displays it on the live video.

FPS represents the number of frames processed per second.

Higher FPS → smoother real-time tracking
Lower FPS  → slower visual response

This gives a simple performance metric while the application is running.

🏗️ System Architecture

┌──────────────────────────────┐
│          USER HAND           │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│         WEBCAM INPUT         │
│      Continuous Video        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│           OpenCV             │
│ Frame Capture & Processing   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│       MediaPipe Hands        │
│     Hand Landmark Detection  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Landmark Coordinates     │
│       & Hand Structure       │
└──────────────┬───────────────┘
               │
          ┌────┴────┐
          ▼         ▼
┌──────────────┐ ┌──────────────┐
│ Draw/Highlight│ │ Print/Process│
│  Landmarks    │ │ Coordinates  │
└──────┬───────┘ └──────┬───────┘
       │                │
       └───────┬────────┘
               ▼
┌──────────────────────────────┐
│       FPS Calculation        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      LIVE VIDEO OUTPUT       │
└──────────────────────────────┘

🔄 Complete Project Workflow

START
  │
  ▼
Initialize Webcam
  │
  ▼
Capture Frame
  │
  ▼
Process Frame with OpenCV
  │
  ▼
Detect Hands with MediaPipe
  │
  ▼
Are Hands Detected?
  │
  ├── No ──────────────► Continue Reading Frames
  │
  └── Yes
       │
       ▼
   Extract Landmarks
       │
       ▼
   Read Coordinates
       │
       ▼
   Draw Landmarks
       │
       ▼
 Highlight Landmark 0
       │
       ▼
 Calculate FPS
       │
       ▼
 Display Live Feed
       │
       ▼
 Repeat

🧠 Hand Tracking Logic

The project can be understood through four major stages:

Stage 1 — Capture

OpenCV obtains the live image from the webcam.

Stage 2 — Detect

MediaPipe processes the frame and identifies available hand landmarks.

Stage 3 — Visualize

The detected landmarks are drawn over the original frame and landmark 0 is highlighted.

Stage 4 — Measure

The application calculates FPS to monitor real-time processing performance.

🗂️ Project Structure

The original project instructions reference the following core files:

Hand-Tracking-Using-Opencv/
│
├── app.py
│   └── Main Python application
│
├── requirements.txt
│   └── Python dependency list
│
└── README.md
    └── Project documentation

Keep any additional files, folders, media, or configuration files that already exist in your repository. The structure above documents the files explicitly referenced by the supplied project README.

🛠️ Technology Stack

Technology

Purpose

🐍 Python

Main programming language

👁️ OpenCV

Webcam capture, image processing and video display

✋ MediaPipe

Hand detection and landmark tracking

📦 pip / requirements.txt

Dependency installation and environment setup

📦 Installation & Setup

Step 1 — Clone the Repository

git clone https://github.com/keshavkapill/Hand-Tracking-Using-Opencv.git
cd Hand-Tracking-Using-Opencv

Step 2 — Create a Virtual Environment

A virtual environment is recommended to keep project dependencies isolated.

Using Python venv

python -m venv venv

Activate it on Windows:

venv\Scripts\activate

Using Conda

conda create -p ./venv python=3.x -y
conda activate ./venv

Step 3 — Install Dependencies

Install the dependencies listed in the project:

pip install -r requirements.txt

The primary libraries used are:

OpenCV
MediaPipe

▶️ Running the Project

Start the application using:

python app.py

The application should initialize the default webcam and begin processing the live video stream.

🖥️ Expected Output

When the application is running, the live camera window provides real-time visual feedback.

The output includes:

✋ Detected Hand

The detected hand is tracked through its landmarks.

📍 Landmark Coordinates

The application prints the coordinates of the detected landmarks.

🟢 Landmark 0

The first landmark is visually emphasized with a filled circle.

⚡ FPS

The current frame-processing rate is displayed on the live feed.

🧪 Functional Breakdown

Input
│
└── Webcam Video

Processing
│
├── OpenCV
│   ├── Capture Frame
│   ├── Process Frame
│   └── Display Frame
│
└── MediaPipe Hands
    ├── Detect Hand
    └── Locate Landmarks

Output
│
├── Landmark Visualization
├── Landmark Coordinates
├── Highlighted Landmark 0
└── FPS

🌐 Potential Applications

The tracking foundation created in this project can be extended into several practical applications.

🕹️ Gesture-Controlled Systems

Detected hand landmarks can be used to recognize gestures and control applications.

🎮 Gaming

Hand movements can become input for interactive games.

🥽 Virtual / Augmented Reality

Hand tracking can support natural interaction inside immersive environments.

♿ Accessibility Interfaces

Hand gestures can provide alternative interaction mechanisms.

🖥️ Human-Computer Interaction

The system can act as a foundation for touchless interfaces and gesture-based controls.

🚀 Possible Extensions

The existing hand-tracking pipeline can be expanded into more advanced applications:

Hand Tracking
      ↓
Finger Detection
      ↓
Gesture Recognition
      ↓
Gesture Classification
      ↓
Action Mapping
      ↓
Application Control

Possible additions include:

☝️ Finger counting

👍 Gesture recognition

🖱️ Virtual mouse

✍️ Air drawing

⌨️ Gesture-based virtual keyboard

🎵 Gesture-controlled media player

🎮 Gesture-based gaming

🤖 Gesture-triggered automation

⚠️ Troubleshooting

Camera Does Not Open

Check whether:

Another application is already using the webcam.

Camera permissions are enabled.

The intended camera device is selected.

Dependencies Fail to Install

Verify that:

python --version

returns a Python version compatible with the dependencies specified by the project's environment.

Then retry:

pip install -r requirements.txt

Low FPS

Real-time performance can be affected by:

System CPU performance

Camera resolution

Frame-processing workload

Number of detected hands

Background complexity

Other applications running on the system

🧠 Concepts Demonstrated

Computer Vision

Real-time video capture

Image/frame processing

Object landmark detection

Visualization

Python

Webcam processing

Loops

Functions

Conditional processing

Coordinate handling

Media Processing

Frame-by-frame analysis

Real-time output

FPS calculation

Human-Computer Interaction

Vision-based interaction

Hand movement tracking

Foundation for gesture-based controls

💡 Why This Project Is Useful

This project demonstrates how a standard webcam can be transformed into an interactive computer-vision input device.

Instead of treating camera footage as simple video, the application extracts structured information from the visual scene:

Camera Feed
     ↓
Visual Information
     ↓
Hand Detection
     ↓
Landmark Data
     ↓
Computer Interaction

That makes the project a useful foundation for moving from basic webcam processing toward gesture recognition and intelligent human-computer interaction.

🔮 Future Development Roadmap

Current
  │
  └── Hand Landmark Tracking
          │
          ▼
      Finger Tracking
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

Potential future improvements include:

Multi-hand gesture recognition

Custom gesture classification

Finger-count detection

Smoother tracking

Gesture-to-command mapping

Coordinate recording

Real-time gesture control

Integration with AI applications

👨‍💻 Developer

<div align="center">

Keshav Kapil

Computer Science student interested in Software Development, Data Analytics, Cloud Computing, Computer Vision, and Full-Stack Development.

</div>

🤝 Connect With Me

<div align="center">

<a href="https://github.com/keshavkapill">
  <img src="https://img.shields.io/badge/GitHub-Keshav%20Kapil-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="https://www.linkedin.com/in/keshavkapil15/">
  <img src="https://img.shields.io/badge/LinkedIn-Keshav%20Kapil-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<br><br>

<a href="https://github.com/keshavkapill">
  <b>GitHub Profile</b>
</a>
&nbsp;&nbsp;•&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/keshavkapil15/">
  <b>LinkedIn Profile</b>
</a>

<br><br>

❤️ Made with Love by Keshav

</div>

<div align="center">

✋ Track • Detect • Visualize • Interact

⭐ Thanks for visiting the project!

</div>
