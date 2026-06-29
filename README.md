# eBot Waypoint Navigation & Path Planning

An autonomous navigation system developed for the eBot robotics platform. This project implements a precise path-planning script that commands the robot to sequentially traverse a series of pre-defined waypoints across a 2D plane, ensuring exact orientation profiling at each goal location.

## 🚀 Features
* **Sequential Waypoint Traversal:** Executes multi-point navigation routines continuously across a designated map or space.
* **Full Pose Alignment:** Targets precise spatial coordinates $(X, Y)$ while simultaneously calculating and aligning to the required orientation ($\text{Yaw}$).
* **Real-time Odometry Tracking:** Monitors and corrects heading errors during transit to ensure high accuracy between nodes.

## 🛠️ System & Tech Stack
* **Language:** Python 3.x
* **Core Concepts:** Differential Drive Kinematics, Odometry, Coordinate Transformation, Closed-loop Control.
* **Target Hardware:** eBot Mobile Robot Platform.

## 📂 Project Structure
* `navigation_script.py` - Core Python execution script hosting the waypoint sequence array and the movement control loop.
* `README.md` - Documentation of system design and execution.

## 📋 How It Works
1. **Pose Matrix Definition:** Waypoints are supplied to the navigation controller as an array of target states: $[X_i, Y_i, \text{Yaw}_i]$.
2. **Heading Correction:** The robot calculates the distance and angle relative to the upcoming waypoint.
3. **Linear & Angular Control:** Closed-loop velocity feedback adjusts wheel speeds to reach the target location within defined tolerance thresholds.
4. **Final Rotation:** Upon reaching the physical $X,Y$ coordinate, the robot spins in place to match the specific target $\text{Yaw}$ orientation before transitioning to the next objective.

## 🔧 Installation & Usage
1. Clone the repository directly to your workspace:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/ebot-waypoint-navigation.git](https://github.com/YOUR_USERNAME/ebot-waypoint-navigation.git)
