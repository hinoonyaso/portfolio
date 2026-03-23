# Robotics / AI Portfolio - 남상기

로봇 SW 채용 관점에서 빠르게 검토할 수 있도록, 이 저장소는 **프로젝트 인덱스 허브** 역할에 집중합니다.

- Focus: ROS2 / Nav2 기반 AMR 주행 안정화, 센서 정합, 임베디드 통신 신뢰성
- Role Target: Robot Software Engineer (Autonomous Navigation / Embedded Control)
- Contact: hinoonyaso@gmail.com

## Featured Project

### 1. AI Secretary Robot (Flagship)
오프라인 음성비서 + 자율주행 로봇 통합 프로젝트 (핵심 메인 프로젝트)

- Repo: https://github.com/hinoonyaso/AI_secretary_robot
- Tech: ROS2, Nav2, Voice AI, Jetson, Embedded Integration
- Key Results:
  - STT -> Intent -> LLM -> Robot Action 파이프라인 기반 음성 로봇 제어 시스템
  - 로봇 주행/응답 파이프라인 통합
  - 실사용 중심 기능 검증 및 고도화 진행

### 2. ROS2 기반 자율주행 신발 피킹 로봇 (스마트 물류)
협소 복도 주행 안정화와 정밀 정차를 지표로 검증한 ROS2 프로젝트

- Repo: https://github.com/addinedu-ros-8th/ros-repo-3.git
- Tech: ROS2, Nav2(TEB), TF2, ArUco, micro-ROS, ESP32
- Key Results:
  - CTE RMS 30%↓
  - Replan latency 40%↓
  - Precision stop error ±5cm

**Demo**
- Image: <img width="360" height="320" alt="image" src="https://github.com/user-attachments/assets/2422b2f3-911b-45ab-adce-ad6af130e279" />
         <img width="480" height="320" alt="image" src="https://github.com/user-attachments/assets/50998c64-a21b-48cc-831c-6161c4840a27" />

- GIF: ![Dashboard Image 2](https://github.com/user-attachments/assets/1f6ed6ce-8fd7-4b66-a0e9-99cd54573325)

## Projects

### 3. COOLRO - Autonomous Golf Caddie Robot
실시간 사람 추종 + STM32 PID 조향 제어 + AI 스윙 분석

- Repo: https://github.com/hinoonyaso/coolro.git
- Tech: Raspberry Pi, MediaPipe Pose, OpenCV CLAHE, UART, STM32 PID, Flutter, Firebase, AWS EC2
- Key Results:
  - PID 연속 조향으로 이산 명령 대비 조향 정밀도 향상 (STM32 100Hz 실시간 루프)
  - 초음파 중앙값 필터로 거리 측정 노이즈 제거
  
**Demo**
- Image: <img width="240" height="320" alt="image" src="https://github.com/user-attachments/assets/6eeffc94-96bc-4c62-91b5-f38999e69a78" />
         <img width="240" height="320" alt="image" src="https://github.com/user-attachments/assets/14d1551c-eb2d-46f0-a517-eca4d078a518" />
- Video:
<p>
  <a href="video/motor.MP4">
    <img src="video/motor.jpg" width="240">
  </a>
  <a href="video/coolro.mp4">
    <img src="video/coolro.png" width="240">
  </a>
</p>

### 4. Robot Arm Vision Project
비전 기반 로봇암 제어/작업 자동화 프로젝트

- Repo: https://github.com/hinoonyaso/robot_arm_project.git
- Tech: Robot Arm Control, Computer Vision, Embedded Integration

**Demo**
- Video(main,vision):
<p>
  <a href="video/robot_arm.mp4">
    <img src="video/robot_arm.png" width="240">
  </a>
  <a href="video/robot_arm_vision.mp4">
    <img src="video/robot_arm_vision.png" width="240">
  </a>
</p>

### 5. Smart Pill Dispenser (Face ID + IoT)
얼굴 인증 + 스케줄 기반 자동 복약 분배 시스템

- Repo: https://github.com/addinedu-ros-8th/iot-repo-1.git
- Tech: FaceNet512, TCP, MySQL, Raspberry Pi, Arduino, Servo Control
- Key Results:
  - Authentication success +15%p
  - Log miss rate below 0.5%

**Demo**
- Image: <img width="480" height="320" alt="image" src="https://github.com/user-attachments/assets/43307eeb-95e0-4b6f-9393-57b2177ad22a" />
- Video: <a href="video/pillguy.MOV">
  <img src="video/pillguy.png" width="240">
</a>

### 6. Fitness AI Trainer (Edge AI)
실시간 자세 인식/피드백 지연 최적화

- Repo: https://github.com/addinedu-ros-8th/deeplearning-repo-1.git
- Tech: MediaPipe, TensorFlow/Keras, LSTM, PyQt
- Key Results:
  - Frame drop 30%↓
  - Feedback latency 120ms -> 50ms

**Demo**
- Image: <img width="360" height="320" alt="image" src="https://github.com/user-attachments/assets/9f5bc563-48d2-4f2f-a051-13c8078c4413" />
         <img width="240" height="320" alt="image" src="https://github.com/user-attachments/assets/ac5468d4-d11f-4a27-bfcb-eae8ae294609" />
         <img width="240" height="320" alt="image" src="https://github.com/user-attachments/assets/08c8d1c9-9b3f-44e1-a2b1-480d6fcea4af" />

- GIF: ![Image](https://github.com/user-attachments/assets/fc12cd22-ef3a-408d-b2a1-71b10ff9d416)

## Tech Stack

Robotics
ROS2, Nav2, SLAM Toolbox, TF2

Embedded
STM32, ESP32, UART, micro-ROS

AI / CV
MediaPipe, OpenCV, TensorFlow, YOLO

Infrastructure
Linux, Docker, TCP/IP, MySQL

## Notes

- 이 저장소는 포트폴리오 인덱스입니다.
- 상세 설계/코드/재현 방법은 각 프로젝트 저장소 README에서 확인할 수 있습니다.
