# MacAEV – McMaster Autonomous Electrified Vehicle 🚗⚡

A real-time embedded control and autonomous navigation system for a 1/10th scale electric RC vehicle. Developed using ROS on a Jetson Nano, the system integrates LiDAR and IMU-based localization, mapping, and control algorithms to enable manual, semi-autonomous, and fully autonomous driving modes.

- 📚 **Overview:https://github.com/GitMustafaCode/Autonomous-Electric-Vehicle-System/blob/main/Overview.png**  
---

## 🔥 Key Features

- ✅ **ROS-based architecture** running on Jetson Nano
- ✅ **LiDAR + IMU-based localization**
- ✅ **Grid Occupancy Mapping**
- ✅ **Feedback-linearizing + PD controller** for wall following
- ✅ **Virtual barrier generation** using Quadratic Optimization
- ✅ **Manual & Autonomous driving modes**
- ✅ (Bonus) **RGB-D camera integration** for enhanced obstacle detection

---

## 🛠️ Hardware Overview

- **RC Platform:** ARMA GRANITE 4x4 (1/10 scale)
- **Onboard Computer:** NVIDIA Jetson Nano
- **Motor Controller:** TRAMPA VESC 6 MkV
- **Sensors:**
  - RPLIDAR A2 (2D LiDAR)
  - BNO055 IMU (9 DOF)
  - Intel RealSense D435i (optional - RGB-D)
- **Battery:** VENOM 3S LiPo
- **Connectivity:** USB, UART, WiFi

---

## 💻 Software Stack

- **OS:** Ubuntu 18.04 LTS
- **ROS:** Melodic
- **Languages:** Python, C++
- **Simulator:** F1TENTH (for safe algorithm development)
- **Libraries:** OpenCV, NumPy, Matplotlib, Open3D
- **Tools:** VESC Tool, JetPack SDK

---

## 🧠 Project Structure

The system was built over 8 iterative modules:

1. Linux command-line & ROS setup on Jetson Nano  
2. Hardware testing & udev configuration  
3. VESC programming and ESC control via ROS  
4. Manual driving and odometry calibration  
5. Localization using LiDAR + IMU  
6. Mapping with occupancy grids  
7. PD + feedback-linearizing controller  
8. (Bonus) RGB-D integration using RealSense camera  

Each component was tested in simulation (F1TENTH) before deployment on the physical vehicle.

---

## 🚀 Getting Started

### Prerequisites

- Jetson Nano running Ubuntu 18.04
- ROS Melodic installed
- RPLIDAR A2 + VESC 6 + optional RGB-D camera
- Python 3.8+
- Required Python packages:

```bash
pip install numpy matplotlib open3d
```

---

### Launching the System

Clone the repository and launch the main ROS stack:

```bash
git clone https://github.com/YourUsername/MacAEV.git
cd MacAEV
roslaunch macaev_control macaev_main.launch
```

---

## 📁 Project Structure

```
.
├── macaev_control/       # Control algorithms
├── macaev_localization/  # Sensor fusion and odometry
├── macaev_mapping/       # Mapping algorithms
├── macaev_vision/        # RGB-D processing (bonus)
├── macaev_launch/        # ROS launch files
├── scripts/              # Calibration and testing scripts
├── docs/                 # Diagrams and images
└── README.md
```

---

## 📄 Resources

- 🧠 **Project Overview Slides:**  
  [📎 https://github.com/GitMustafaCode/Autonomous-Electric-Vehicle-System/blob/main/MacAEV_Overview.pptx

- 📚 **Course Outline:**  
  [📎 ELECENG 3EY4 Course Outline (Winter 2025)](./docs/2025_01_02_ElecEng_3EY4_outline_Winter2025.pdf)

---

