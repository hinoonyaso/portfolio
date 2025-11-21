
# Robot Software & Embedded Portfolio – 남상기

![ROS2](https://img.shields.io/badge/ROS2-Humble-blue)
![Embedded](https://img.shields.io/badge/Embedded-STM32-green)
![AI](https://img.shields.io/badge/AI-Vision-orange)
![Lang](https://img.shields.io/badge/Language-C++%20%7C%20Python-lightgrey)

---

## 🧑‍💻 About

Robot Software & Embedded engineer focusing on **perception–decision–control** pipelines running on real hardware.  
Experienced with ROS2, embedded controllers (STM32), and AI-based vision (YOLO, MediaPipe) on edge devices.

---

## 🧩 Architecture Overview (Mermaid)

```mermaid
flowchart TD
    subgraph Sensing
        Cam[RGB-D Camera]
        Lidar[LiDAR]
        Imu[IMU]
    end

    subgraph AI[Vision & AI]
        Yolo[YOLO Detector]
        MP[MediaPipe Pose Estimator]
    end

    subgraph Nav[SLAM & Navigation]
        SLAM[SLAM Node]
        Planner[Global & Local Planner (DWA)]
    end

    subgraph Ctrl[Control & Embedded]
        Decision[Decision Node]
        STM32[STM32 Controller]
        Motor[Motor Driver]
    end

    subgraph Cloud[Server / Logging]
        Logger[Log Server]
        Monitor[Monitoring / Dashboard]
    end

    Cam --> AI
    Lidar --> SLAM
    Imu --> SLAM
    AI --> Decision
    SLAM --> Planner
    Planner --> Decision
    Decision --> STM32
    STM32 --> Motor
    Decision --> Logger
    Logger --> Monitor
```

---

## 🚀 Projects

### 1️⃣ COOLRO – Autonomous Following Golf Caddy Robot

**Tech Stack**: MediaPipe, OpenCV, Raspberry Pi, STM32, UART, PWM, Flutter  

- Implemented pose-based golf swing analysis using MediaPipe.  
- Estimated distance between user and robot via camera and simple geometry.  
- Designed UART-based real-time motor control between Raspberry Pi and STM32.  
- Solved motor driver instability via power stabilization and PWM tuning.  
- Developed a Flutter app for live video streaming and UX.  
- Performed multiple field tests to reduce tracking delay and distance error.  

📸 *[COOLRO image placeholder]*  
🎥 *[COOLRO demo video link]*  

---

### 2️⃣ ROS2 Autonomous Navigation Robot

**Tech Stack**: ROS2, Nav2, LiDAR, IMU, TF, C++  

- Built LiDAR + IMU-based SLAM with Nav2.  
- Configured DWA local planner for obstacle avoidance in indoor environments.  
- Designed TF tree and sensor frames for consistent pose estimation.  
- Tuned costmap and planner parameters using real-world log data.  

Key files (example):  

- `launch/slam.launch.py` – SLAM launch configuration  
- `config/nav2_params.yaml` – Navigation and planner parameters  
- `src/tf_broadcaster.cpp` – TF broadcaster implementation  

---

### 3️⃣ IoT + Edge Vision System

**Tech Stack**: Python, TCP/Serial, YOLO, MediaPipe, Edge device  

- Implemented TCP/Serial-based sensor streaming from edge device to server.  
- Ran YOLO/MediaPipe on edge to reduce latency and bandwidth.  
- Designed JSON-based protocol for data exchange.  
- Logged and visualized system status for debugging and monitoring.  

---

### 4️⃣ Robot Service Planning (AIROVER / Sensor System)

Planning-focused projects (no hardware implementation) covering:  

- Problem definition & requirement analysis for indoor service robots.  
- Sensor configuration (LiDAR, RGB-D, IMU, ToF) and algorithm mapping (SLAM, DWA, YOLO).  
- Service UX scenarios and state diagrams.  
- High-level architecture and data flow documentation.  

---

## 🔧 Example Code Snippets

### ROS2 – TF Broadcaster

```cpp
geometry_msgs::msg::TransformStamped t;
t.header.stamp = this->get_clock()->now();
t.header.frame_id = "base_link";
t.child_frame_id = "lidar";
// populate translation & rotation...
```

### STM32 – UART Motor Control

```c
HAL_UART_Receive_IT(&huart2, rxBuffer, 1);
motor_set_speed(left_speed, right_speed);
```

### YOLO – Inference Pipeline

```python
results = model(frame)
boxes = results.xyxy[0]
```

---

## 🛠 Tech Stack

- **Languages**: C++, Python  
- **Frameworks**: ROS2 (Nav2, TF), OpenCV, Flutter  
- **Embedded**: STM32, UART, PWM, GPIO  
- **AI / Vision**: YOLO, MediaPipe  
- **Hardware**: LiDAR, IMU, RGB-D Camera, Motor Driver, Raspberry Pi  

---

## 📫 Contact

- GitHub: https://github.com/  
- Email:  
