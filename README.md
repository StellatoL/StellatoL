<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1,11,20&height=200&section=header&text=Hi%2C%20I'm%20Stellato%20%F0%9F%91%8B&fontSize=44&fontAlignY=36" width="100%"/>

  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=38BDF8&center=true&vCenter=true&width=560&lines=STM32+firmware+%E2%86%92+ARM+Linux+%E2%86%92+ROS+2+robotics;FPGA+PCIe+DMA+%2B+NPU+edge+inference;Edge+compute+meets+the+physical+world" alt="Typing SVG" />

  <p align="center">
    <b>Embedded Software Engineer &nbsp;|&nbsp; Robotics &amp; Edge AI &nbsp;|&nbsp; Lifelong Learner</b>
  </p>

  <p align="center">
    <a href="https://en.cppreference.com/w/c"><img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black" alt="C" /></a>
    <a href="https://isocpp.org/"><img src="https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" alt="C++17" /></a>
    <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" /></a>
    <a href="https://docs.ros.org/en/jazzy/"><img src="https://img.shields.io/badge/ROS_2-Jazzy-22314E?style=flat-square&logo=ros&logoColor=white" alt="ROS 2" /></a>
    <a href="https://www.st.com/"><img src="https://img.shields.io/badge/STM32-Bare--metal-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white" alt="STM32" /></a>
    <a href="https://opencv.org/"><img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" /></a>
    <a href="https://www.linux.org/"><img src="https://img.shields.io/badge/Linux-ARM64-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" /></a>
  </p>

</div>

---

## 🔧 Tech Stack

| Domain | Focus & Technologies |
| :--- | :--- |
| **Languages** | `C` · `C++17` · `Python` · `Verilog RTL` · `Shell` |
| **Hardware & Firmware** | `STM32 (Bare-metal)` · `FPGA (PCIe DMA / BAR0, video processing)` · `Motor PID` · `IMU / Kalman` |
| **Edge Compute & Systems** | `RK3568 / ARM64 Linux` · `RKNN NPU` · `Zero-copy Ring Buffer` · `IPC (Shared Memory)` |
| **Robotics & Autonomy** | `ROS 2 Jazzy` · `Nav2` · `Gazebo` · `SLAM / AMCL` · `RGB-D / Semantic Costmaps` |
| **Tools & Vision** | `CMake` · `Qt5 / PyQt6` · `OpenCV` · `Git` · `USB3 Vision` · `ModelSim / PDS` |

---

## 📦 Featured Projects

#### 🚙 [`FPGARACE_2026_Pango_3`](https://github.com/StellatoL/FPGARACE_2026_Pango_3) · Private

> **Four-camera FPGA bird's-eye view and RK3568 ADAS prototype**

- **FPGA video pipeline** — RGB565 frame reads, coordinate mapping, bilinear interpolation, gain and seam blending, and raster reordering; verified in simulation and synthesis.
- **ARM application** — Qt 5 video display with RKNN vehicle/traffic detection, conventional lane detection, short-term tracking, and on-screen ADAS alerts.
- **Current boundary** — The FPGA panorama and ARM application are still separate validation tracks; the complete camera-to-display board pipeline is pending integration and real-stream testing.

`Verilog` `C++17` `Qt5` `RKNN` `OpenCV` `ModelSim` · [Project README](https://github.com/StellatoL/FPGARACE_2026_Pango_3#readme) (access required)

#### 🚗 [`pango-fpga-2026`](https://github.com/StellatoL/pango-fpga-2026) · Private

> **FPGA + RK3568 PCIe heterogeneous intelligent traffic perception system**

- **System architecture** — A three-thread Qt5 concurrent pipeline (capture / inference / UI) driven by a producer–consumer queue that drops frames on overflow.
- **High-speed interconnect** — A zero-copy ring buffer built on FPGA PCIe DMA with a BAR0 register protocol.
- **Edge deployment** — End-to-end YOLOv5 + LPRNet licence-plate recognition on the RKNN NPU, with NEON acceleration and optimised NMS post-processing.

`Verilog` `C++` `Qt5` `PCIe DMA` `RKNN` `ARM64`

#### 🤖 [`vln-logistics-robot`](https://github.com/StellatoL/vln-logistics-robot) · Private

> **Vision-language-navigation (VLN) autonomous logistics robot**

- **ROS 2 architecture** — Six-package workspace with a hand-written modular Nav2 launch, switching seamlessly between SLAM mapping and AMCL localisation.
- **Chassis control** — STM32F407 mecanum-wheel firmware with four-wheel velocity-loop PID and wheel-odometry + IMU fused localisation.
- **Current stage** — Gazebo navigation, RGB-D perception and object-level semantic mapping are in simulation; the Jetson–STM32 ROS 2 serial bridge remains to be built.

`ROS 2 Jazzy` `Nav2` `SLAM` `STM32` `Gazebo` `RGB-D`

#### 🎯 [`RM2026_Buff_verify`](https://github.com/StellatoL/RM2026_Buff_verify) · Private

> **RoboMaster power-rune auto-aim and vision solver**

- **Vision solver** — OpenCV detection, coordinate transforms, ballistic compensation and ROS 2 integration; camera frames come from an external driver.
- **Target prediction** — A competition-rule state machine, sinusoidal angular-velocity fitting and an EKF-based pose filter support aiming at the rotating rune.

`C++17` `ROS 2` `OpenCV` `Ceres Solver` `State Machine`

#### 📡 [`FPGARACE_2025_Gowin_3`](https://github.com/StellatoL/FPGARACE_2025_Gowin_3)

> **Full-stack host software for a Gowin FPGA multi-protocol debugger**

- **High-speed streaming** — A PyQt6 + PyQtGraph oscilloscope reading a 25 Msps ADC, with time-domain waveforms and a live FFT spectrum.
- **Low-level transport** — A high-performance C++ Winsock UDP receiver forwarding data over shared memory (IPC).
- **Protocol decoding** — Hardware-level UART / I²C / SPI / PWM / CAN bus timing decode.

`PyQt6` `C++` `Winsock UDP` `Shared Memory` `FFT`

> Some project repositories are private. Their links are available to collaborators with access.

---

## 🌱 Engineering Focus & Roadmap

<details open>
<summary><b>✅ Core Capabilities</b></summary>
<br/>

- **Bare-metal firmware** — STM32 multi-loop velocity PID, Kalman attitude estimation, fused wheel-odometry + IMU localisation
- **Concurrency & data paths** — producer–consumer queues, ring buffers, PCIe DMA / BAR0 register interaction
- **Host tooling & instrumentation** — PyQt6 + PyQtGraph oscilloscope (time domain / FFT), high-speed C++ UDP receiver, shared-memory IPC
- **ROS 2 navigation stack** — modular hand-written Nav2 launch, SLAM / AMCL dual-mode switching, six-package workspace architecture

</details>

<details open>
<summary><b>🚧 Exploring & Building</b></summary>
<br/>

- **Edge AI acceleration** — RKNN model deployment and runtime profiling on RK3568
- **FPGA–ARM integration** — connect the four-camera panorama pipeline to the ARM application and validate real-stream latency on the board
- **Autonomous exploration** — coverage path planning with incremental replanning, frontier exploration, 45° slope point-cloud filtering on a real chassis
- **Semantic mapping** — YOLOv8 + RGB-D fusion into 2.5D semantic costmaps

</details>

---

## ⚡ Engineering Philosophy

> 💡 *"From STM32 PWM waveforms all the way up to a ROS 2 navigation stack — the most fascinating moment is when register states, timing constraints and neural-network inference finally line up on the same board."*

---

## 📊 GitHub Analytics

<div align="center">

  <img height="180em" src="./profile-summary-card-output/github_dark/3-stats.svg" alt="GitHub Stats" />
  <img height="180em" src="./profile-summary-card-output/github_dark/1-repos-per-language.svg" alt="Top Languages in Public Repositories" />

</div>

<p align="center"><sub>Cards are generated from activity visible to the profile workflow and refreshed daily.</sub></p>

<br/>

### 🐍 Contribution Activity

<div align="center">

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake.svg">
    <img alt="github contribution snake" src="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake.svg" width="100%">
  </picture>

</div>

---

## 📫 Let's Connect

<div align="center">

  <a href="mailto:X1255900804@163.com">
    <img src="https://img.shields.io/badge/Email-X1255900804@163.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
  &nbsp;
  <a href="https://stellatol.github.io/">
    <img src="https://img.shields.io/badge/Blog-stellatol.github.io-4A90E2?style=flat-square&logo=githubpages&logoColor=white" alt="Blog" />
  </a>
  &nbsp;
  <a href="https://github.com/StellatoL">
    <img src="https://img.shields.io/badge/GitHub-@StellatoL-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
  </a>

  <br/><br/>

  <sub>⭐️ Thanks for stopping by · Always building, always exploring</sub>

</div>
