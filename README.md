# McMaster Autonomous Electrified Vehicle (AEV)

An embedded control and autonomous navigation system for a 1/10th scale electrified RC car. The project integrates electric propulsion, LiDAR-based obstacle detection, real-time localization, and feedback control to enable semi- and fully autonomous driving modes.

---

📄 **Complete Project Overview**  
Read our full technical report explaining the system design, implementation, and testing:  
https://github.com/GitMustafaCode/Autonomous-Electric-Vehicle-System/blob/main/Overview.png

---

## 🚗 Demonstration

### Setup  
<img src="docs/images/aev_setup.jpg" alt="AEV Setup" width="500"/>

### Autonomous Driving through Virtual Barriers  
<img src="docs/images/aev_drive_1.jpg" alt="AEV Drive 1" width="300"/>  
<img src="docs/images/aev_drive_2.jpg" alt="AEV Drive 2" width="300"/>

---

## 🔌 System Overview

This embedded system uses a **Jetson Nano** running **ROS** to control the McMaster AEV platform in both manual and autonomous modes. The system integrates:

- **Electric Propulsion Control (VESC-based)**
- **LiDAR & Odometry-based Localization**
- **Mapping & Grid Occupancy Algorithms**
- **PD + Feedback-Linearizing Control**
- **Quadratic Optimization for Virtual Barriers**
- **(Bonus) RGB-D Camera for Enhanced Mapping**

---

## 🧰 Getting Started

### Prerequisites

- NVIDIA Jetson Nano Developer Kit  
- VESC-compatible Electronic Speed Controller  
- 360° 2D LiDAR (e.g., RPLiDAR A1/A2)  
- RGB-D Camera (e.g., Intel RealSense D435 – optional)  
- ROS Noetic on Ubuntu 20.04  
- Python 3.8+  
- Required Libraries: `rospy`, `numpy`, `matplotlib`, `open3d`

---

### Hardware Setup

- Connect **LiDAR** to Jetson Nano via USB.  
- Connect **VESC** via UART to Jetson.  
- Power the propulsion system through the **battery circuit**.  
- Mount the **RGB-D camera** (if used) on the front chassis.  
- Ensure the **Jetson Nano is flashed and ROS is installed**.

---

### Software Setup

Clone this repository:

```bash
git clone https://github.com/YourUsername/AEV-Autonomous-Car.git
cd AEV-Autonomous-Car
```

Install required Python packages:

```bash
pip install numpy matplotlib open3d
```

Run the launch file to bring up the control system:

```bash
roslaunch aev_system aev_main.launch
```

---

## 🧠 How It Works

### Manual Control & Calibration
The vehicle can be manually controlled for testing. Odometry is calibrated using wheel encoder and LiDAR data.

### Localization & Mapping
A Grid Occupancy Mapping algorithm is developed using LiDAR, IMU, and wheel odometry data.

### Autonomous Navigation
Virtual barriers are constructed using Quadratic Optimization. A PD + feedback-linearizing controller keeps the vehicle between the barriers.

### Bonus - RGB-D Integration
Depth data from the RGB-D camera is fused with LiDAR data to enhance obstacle detection and mapping.

---

## 📁 Code Structure

```
.
├── aev_control/            # Autonomous control algorithms
├── aev_localization/      # Localization and mapping nodes
├── aev_launch/            # ROS launch files
├── aev_vision/            # RGB-D camera integration (bonus)
├── scripts/               # Python scripts for testing and visualization
├── docs/                  # Images and diagrams
└── README.md
```

---

## ✅ Features

✔️ VESC Motor Control with ROS  
✔️ Real-Time Localization with LiDAR and IMU  
✔️ Autonomous Navigation using Virtual Barriers  
✔️ PD + Feedback-Linearizing Controller  
✔️ Optional RGB-D Stereo Vision Module  
✔️ Modular ROS Nodes for Scalability
