# McMaster Autonomous Electrified Vehicle (AEV)

An embedded control and autonomous navigation system for a 1/10th scale electrified RC car. The project integrates electric propulsion, LiDAR-based obstacle detection, real-time localization, and feedback control to enable semi- and fully autonomous driving modes.

---

📄 **Complete Project Report**  
Read our full technical report explaining the system design, implementation, and testing:  
[Final Project Report (PDF)](https://github.com/YourUsername/AEV-Autonomous-Car/blob/main/AEV_Final_Report.pdf)

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

