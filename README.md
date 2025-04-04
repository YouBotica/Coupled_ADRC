# Coupled ADRC Controller for Autonomous Racing

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)  
**Active Disturbance Rejection Control (ADRC)** implementation for longitudinal and lateral vehicle control in autonomous racing. Designed for ROS 2 and tested in the Indy Autonomous Challenge.

## 📝 Overview
This repository contains a **Coupled ADRC** controller that combines:
- **Longitudinal control** (throttle/brake via traction force calculation)
- **Lateral control** (steering via yaw rate tracking and path following)  

The controller uses Extended State Observers (ESOs) to estimate and reject disturbances (e.g., tire slip, model inaccuracies).

## 🚀 Features
- **Coupled Dynamics Handling**: Simultaneously controls speed and steering using vehicle dynamics feedback
- **Disturbance Estimation**: Kalman-filter-based ESOs to estimate unmodeled dynamics
- **Path Tracking**: Adaptive lookahead distance based on current speed
- **Real-Time Safe**: Includes saturation limits for steering/throttle commands
- **ROS 2 Integration**: Subscribes to odometry, path, and velocity topics; publishes control commands

## 📦 Dependencies
- **ROS 2** (Foxy/Humble tested)
- `Eigen3` (for matrix operations)
- `nav_msgs`, `std_msgs`, `geometry_msgs`
- Vehicle-specific parameters (e.g., mass, tire stiffness)

## 🛠️ Installation
1. Clone into your ROS 2 workspace:
   ```bash
   git clone https://github.com/your-repo/coupled_adrc.git




