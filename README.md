<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1,11,20&height=200&section=header&text=Hi%2C%20I'm%20StellatoL%20%F0%9F%91%8B&fontSize=44&fontAlignY=36" width="100%"/>

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
| **Hardware & Firmware** | `STM32 (Bare-metal)` · `FPGA (PCIe DMA / BAR0)` · `Motor PID` · `IMU / Kalman` |
| **Edge Compute & Systems** | `RK3568 / ARM64 Linux` · `RKNN NPU` · `Zero-copy Ring Buffer` · `IPC (Shared Memory)` |
| **Robotics & Autonomy** | `ROS 2 Jazzy` · `Nav2` · `Gazebo` · `SLAM / AMCL` · `RGB-D / Semantic Costmaps` |
| **Tools & Vision** | `CMake` · `Qt5 / PyQt6` · `OpenCV` · `Git` · `USB3 Vision` |

---

## 📦 Featured Projects

#### 🚗 [`pango-fpga-2026`](https://github.com/StellatoL/pango-fpga-2026)

> **FPGA + RK3568 PCIe heterogeneous intelligent traffic perception system**

- **System architecture** — A three-thread Qt5 concurrent pipeline (capture / inference / UI) driven by a producer–consumer queue that drops frames on overflow.
- **High-speed interconnect** — A zero-copy ring buffer built on FPGA PCIe DMA with a BAR0 register protocol.
- **Edge deployment** — End-to-end YOLOv5 + LPRNet licence-plate recognition on the RKNN NPU, with NEON acceleration and optimised NMS post-processing.

`Verilog` `C++` `Qt5` `PCIe DMA` `RKNN` `ARM64`

#### 🤖 [`vln-logistics-robot`](https://github.com/StellatoL/vln-logistics-robot)

> **Vision-language-navigation (VLN) autonomous logistics robot**

- **ROS 2 architecture** — Six-package workspace with a hand-written modular Nav2 launch, switching seamlessly between SLAM mapping and AMCL localisation.
- **Chassis control** — STM32F407 mecanum-wheel firmware with four-wheel velocity-loop PID and wheel-odometry + IMU fused localisation.
- **Simulation & hardware** — Gazebo physics modelling validated on a real chassis.

`ROS 2 Jazzy` `Nav2` `SLAM` `STM32` `Gazebo` `Sensor Fusion`

#### 🎯 [`RM2026_Buff_verify`](https://github.com/StellatoL/RM2026_Buff_verify)

> **RoboMaster power-rune auto-aim and vision solver**

- **Driver & communication** — Self-written C++17 USB3 Vision driver node for a Hikrobot industrial camera (3072×2048 @ 120Hz), with a 0.60px reprojection calibration error.
- **Target tracking** — A rule state machine combined with a sinusoidal velocity predictor, giving high-precision feed-forward on the rotating rune.

`C++17` `ROS 2` `USB3 Vision` `OpenCV` `State Machine`

#### 📡 [`FPGARACE_2025_Gowin_3`](https://github.com/StellatoL/FPGARACE_2025_Gowin_3)

> **Full-stack host software for a Gowin FPGA multi-protocol debugger**

- **High-speed streaming** — A PyQt6 + PyQtGraph oscilloscope reading a 25 Msps ADC, with time-domain waveforms and a live FFT spectrum.
- **Low-level transport** — A high-performance C++ Winsock UDP receiver forwarding data over shared memory (IPC).
- **Protocol decoding** — Hardware-level UART / I²C / SPI / PWM / CAN bus timing decode.

`PyQt6` `C++` `Winsock UDP` `Shared Memory` `FFT`

---

## 🌱 Engineering Focus & Roadmap

<details open>
<summary><b>✅ Core Capabilities</b></summary>
<br/>

- **Bare-metal firmware** — STM32 multi-loop velocity PID, Kalman attitude estimation, fused wheel-odometry + IMU localisation
- **Concurrency & data paths** — overflow-dropping producer–consumer queues, zero-copy ring buffers, PCIe DMA / BAR0 register interaction
- **Host tooling & instrumentation** — PyQt6 + PyQtGraph oscilloscope (time domain / FFT), high-speed C++ UDP receiver, shared-memory IPC
- **ROS 2 navigation stack** — modular hand-written Nav2 launch, SLAM / AMCL dual-mode switching, six-package workspace architecture

</details>

<details open>
<summary><b>🚧 Exploring & Building</b></summary>
<br/>

- **Edge AI acceleration** — the full ONNX → RKNN deployment path, NEON optimisation of YOLOv5 / LPRNet on the RK3568 NPU
- **Autonomous exploration** — coverage path planning with incremental replanning, frontier exploration, 45° slope point-cloud filtering on a real chassis
- **Semantic mapping** — YOLOv8 + RGB-D fusion into 2.5D semantic costmaps

</details>

---

## ⚡ Engineering Philosophy

> 💡 *"From STM32 PWM waveforms all the way up to a ROS 2 navigation stack — the most fascinating moment is when register states, timing constraints and neural-network inference finally line up on the same board."*

---

## 📊 GitHub Analytics

<div align="center">

  <img src="https://github-readme-stats.vercel.app/api?username=StellatoL&show_icons=true&theme=react&hide_border=true&bg_color=0D1117&include_all_commits=true" width="48.5%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=StellatoL&layout=compact&theme=react&hide_border=true&bg_color=0D1117&langs_count=8" width="48.5%" />

  <br/><br/>

  <img src="https://streak-stats.demolab.com/?user=StellatoL&theme=react&background=0D1117&hide_border=true" width="98%" />

  <br/><br/>

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake.svg">
    <img alt="github contribution snake" src="https://raw.githubusercontent.com/StellatoL/StellatoL/output/github-contribution-grid-snake.svg" width="98%">
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
