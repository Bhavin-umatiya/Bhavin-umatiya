# Bhavin Umatiya

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=28&center=true&vCenter=true&width=600&height=60&duration=4000&lines=FPGA+%2F+Hardware+Acceleration;RTL+Design%26;Embedded+Firmware+(Zephyr%2C+STM32);Upstream+contributor+to+Zephyr%2C+ROS+2%2C+BlackParrot" />
</p>

<p align="center">
  <a href="https://bhavin-umatiya.github.io/Bhavin-portfolio/"><img src="https://img.shields.io/badge/Portfolio-252525?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"/></a>
  <a href="https://www.linkedin.com/in/bhavin-umatiya/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://www.youtube.com/@BAREMETALSS"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube"/></a>
  <a href="mailto:umatiyabhavin@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

## What I build

I design digital hardware and verify it properly. Recent work: a Vision-Transformer accelerator on a Xilinx ZCU104 (300 MHz timing closure, 50.7× over the ARM baseline), a CDC-safe async FIFO with a full UVM 1.2 testbench, and merged fixes in the Zephyr RTOS Bluetooth controller. ECE at Nirma University.

---

## Featured projects

| Project | What it is | Highlights | Stack |
|---|---|---|---|
| **[ZCU104 ViT Hardware Accelerator](https://github.com/Bhavin-umatiya/ZCU104-ViT-Hardware-Accelerator)** | PS/PL-partitioned Vision Transformer inference on Zynq UltraScale+ | Softmax, GELU, LayerNorm as fully pipelined HLS IP over AXI; matmul on the DPU. **72.5 ms vs 3671 ms on ARM (50.7×)**, 300 MHz, 15.4 W. Demo video in repo. | Vitis HLS · Vitis AI · AXI · PYNQ |
| **[Async FIFO + UVM Verification](https://github.com/Bhavin-umatiya/async-fifo-uvm-verification)** | Clock-domain-crossing FIFO with Gray-code pointers and 2-stage synchronizers | Complete UVM 1.2 environment: sequencer/driver/monitor, constrained-random stimulus, SVA, cross functional coverage, reference-model scoreboard. 500-txn regression + directed overflow/underflow tests. | Verilog · SystemVerilog · UVM · XSim |
| **[ZCU104 Adaptive Video Pipeline](https://github.com/Bhavin-umatiya/zcu104-adaptive-video-pipeline)** | Edge-AI surveillance pipeline, fully on-device | YOLOv4 on the DPU drives 3-zone ROI priority masking into hardware H.264 encoding on the VCU — no host processing. | Vitis AI · VCU · GStreamer |
| **[Secure STM32 Bootloader](https://github.com/Bhavin-umatiya/secure-bootloader-stm32-checksum)** | Bare-metal bootloader for STM32 Nucleo | Checksum-verified application image before handoff, fallback path on failure, UART flashing. | Embedded C · STM32 · UART |
| **[AI–VLSI Co-Design](https://github.com/Bhavin-umatiya/AI-VLSI-Feasibility-Engine)** | Multi-agent pipeline that turns a natural-language spec into synthesizable RTL | 3-agent flow with lint/synthesis feedback loop. | SystemVerilog · Python · LLMs |
| **[BharatPart](https://bharatpart.com)** *(side project)* | Parametric electronic-component search and BOM checker for Indian buyers | Aggregates Mouser, DigiKey and Indian distributors with live INR pricing and stock. | Python · Web |

---

## Open-source contributions (merged upstream)

**[Zephyr RTOS](https://github.com/zephyrproject-rtos/zephyr)** — The Linux Foundation
- [#106472](https://github.com/zephyrproject-rtos/zephyr/pull/106472) — **Bluetooth Controller:** introduce timer-tick conversion define; fixes the Nordic Link Layer passing raw microsecond values to `nrf_timer_cc_set()`.
- [#106404](https://github.com/zephyrproject-rtos/zephyr/pull/106404) — **POSIX:** remove redundant unsigned comparison in `pthread_attr_setstack` (Coverity CID 434559).
- [#106403](https://github.com/zephyrproject-rtos/zephyr/pull/106403) — **Docs:** exhaustive in-tree IEEE 802.15.4 radio-driver overview (14 drivers).

**[ROS 2 Controllers](https://github.com/ros-controls/ros2_controllers)** — Open Robotics
- 3 merged PRs in `diff_drive_controller`: removed a deprecated parameter, migrated exception-based init to the ros2_control lifecycle API, fixed a runtime anti-pattern. [All my PRs →](https://github.com/ros-controls/ros2_controllers/pulls?q=is%3Apr+author%3ABhavin-umatiya)

**[BlackParrot RISC-V](https://github.com/black-parrot/black-parrot)** — Bespoke Silicon Group / FOSSi Foundation
- Full Verilator simulation bring-up of the core; merged documentation correction. [My PRs →](https://github.com/black-parrot/black-parrot/pulls?q=is%3Apr+author%3ABhavin-umatiya)

---

## Skills

| | |
|---|---|
| **RTL & verification** | Verilog, SystemVerilog, UVM 1.2, SVA, functional coverage, CDC, STA/timing closure |
| **FPGA / HLS** | Vivado, Vitis HLS, Vitis AI (DPU), AXI4/AXI-Lite/AXI-Stream, Zynq UltraScale+ (ZCU104), Altera DE2 |
| **Embedded** | C, Zephyr RTOS, STM32, ESP32, Teensy, Nordic nRF (BLE), SPI/I2C/UART |
| **Simulation & tools** | XSim, ModelSim/Questa, Verilator, Quartus, Python, Tcl, Git |

---

## Recognition

- **AMD Slingshot — Top 4**, AMD India Campus Days 2026
- **Smart India Hackathon 2025** — campus finalist (200+ teams); 1st place, internal hardware hackathon
- **[BAREMETALSS](https://www.youtube.com/@BAREMETALSS)** — YouTube channel on FPGA design, Vivado workflows and hardware acceleration
