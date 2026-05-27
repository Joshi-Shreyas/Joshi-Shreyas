<div align="center">

# Shreyas Joshi

**MS ECE @ Northeastern University** · Boston, MA · Graduating Dec 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/joshi-shreyas-ece)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:joshi.shreyas@northeastern.edu)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Joshi-Shreyas)

</div>


## About Me

I work at the intersection of **hardware systems and machine learning**, building things that run close to silicon and think with data. My background spans semiconductor equipment engineering, embedded firmware, HPC-scale ML, and computer architecture.

Most recently at **Veeco Instruments** (San Jose), I built hybrid LSTM models for early fault detection on Ion Beam Deposition systems, semiconductor manufacturing equipment:  achieving AUC-PR of 0.91 on rare fault classes. I also designed sensor interfacing circuits for robotic end-effector calibration: hardware and ML, not one or the other.

I think about problems from both ends: what the silicon is doing, and what the model needs to learn.


## Selected Projects

| Project | What it does | Stack |
|---|---|---|
| [CUDA & MPI Parallel Performance Analysis](https://github.com/Joshi-Shreyas/cuda-parallel-performance-analysis) | Coalesced vs non-coalesced CUDA kernel benchmarks on Tesla V100 (5.8× speedup, 640 GB/s peak BW) + distributed MPI histogramming across 1 and 2 HPC nodes — bottleneck isolation via MPI_Scatterv analysis. | CUDA C · OpenMPI · C · Slurm |
| [Plasma Etch Surrogate Model](https://github.com/Joshi-Shreyas/plasma-surrogate) | Neural network digital twin for plasma etch rate prediction across 300mm wafers. 94.19% accuracy, sub-millisecond inference, 1000× speedup over physical solvers. Trained on Northeastern HPC (Slurm). | PyTorch · NumPy · Matplotlib · Slurm |
| LingBot-VA: Vision-Action Robot Control | INT8 quantization of a vision-action transformer for robot manipulation. 49% inference speedup, 17.2% VRAM reduction, 43.8%→87.5% task success on open_microwave benchmark. Evaluated on A100 GPUs. | PyTorch · INT8 Quantization · A100 HPC |
| Parallel Image Segmentation (CPU+GPU) | K-means segmentation with OpenMP + SSE4.2 SIMD. 10.78× speedup, 86.9% energy savings. Extended Amdahl's Law with 2D parallelism model cutting prediction error from 41–52% to 0–7.8%. | C · OpenMP · SIMD · Intel VTune · Roofline |
| Secure ECC Communication | Hybrid ECDH + AES-256 encryption with ECDSA authentication. 100% MITM attack detection. ML-based signature anomaly detection. | Python · ECC · AES-256 |


## Experience Highlights

**Veeco Instruments** · Electrical Engineer Co-op · *Jul–Dec 2025*
> Built hybrid LSTM model on multi-sensor time-series IBD (Ion Beam Deposition) semiconductor equipment data with class balancing:  AUC-PR of 0.91 on rare fault detection · Engineered custom data acquisition and preprocessing pipelines integrating hardware diagnostics with ML analytics for predictive maintenance · Designed I2C-based sensor interfacing circuit for robotic end-effector calibration · Performed diagnostics, calibration, and validation of IBD semiconductor processing equipment · Supported system-level electrical design reviews and hardware specification documentation

**Northeastern University** · Teaching Assistant · *Jan 2025–Present*
> Digital Design & Computer Architecture (EECE 2310) — Promoted from Lab TA to Course + Lab TA · Verilog · FPGA (DE1-SoC, Quartus Prime) · Mentored students through ALUs, binary adders, counters, timing analysis and simulation
> Analysis of Random Phenomena (EECE 3468) — May–Present

**IEEE CASS Bangalore Chapter** · Student Intern · *Oct–Dec 2023*
> CRC-16 error detection in Verilog using LFSR · 2nd Runner-Up, Best Internship Presentation across Karnataka State

**Renalyx Health Systems** · Hardware Intern · *Dec 2022–Jan 2023*
> PCB design and validation in OrCAD · Embedded firmware for Renesas MCUs using E2 Studio · Signal conditioning and power management for biomedical sensors · BOM generation · Hardware validation for dialysis machine · ECO process documentation in a regulated medical device environment

**BHT Technologies** · Product Development Intern · *Oct–Dec 2022*
> Embedded systems on Arduino, ESP32, ESP32-CAM, Teensy · Wireless protocols: Wi-Fi, BLE, MQTT · IoT sensor interfacing and real-time data transmission · C/C++ and Python microcontroller programming


## Tech Stack

```
ML & AI         PyTorch · TensorFlow · Scikit-learn · NumPy · SciPy · OpenCV · INT8 Quantization
GPU & HPC       CUDA · Slurm · OpenMP · SIMD/SSE · OpenMPI · Intel VTune · Roofline Analysis
Systems         x86 · RISC-V · ARM · FPGA (Quartus, Xilinx) · Verilog · VHDL · Linux
Embedded        Arduino · ESP32 · Teensy · I2C · SPI · UART · BLE · MQTT
EDA & Tools     Cadence Allegro · OrCAD · PSpice · ModelSim · SolidWorks
Languages       Python · C/C++ · CUDA C · Java · MATLAB · Bash
Domain          Semiconductor Manufacturing · Plasma Etch · Digital Twins · Predictive Maintenance
```


## Education

**Northeastern University, Boston** · MS Electrical & Computer Engineering · GPA 3.73 · Dec 2026
Concentration: Computer Systems and Software
*Coursework: Deep Learning, Embedded Systems, Machine Learning, High Performance Computing, Computer Architecture, Hardware Security, Data Visualization*

**Bangalore Institute of Technology** · B.E. Electronics & Communication Engineering · GPA 8.89/10 · May 2024


## Publications

- **"A High Speed Memristor Digital Quadrature Clock Generation"** — Patent and Design Journal India, June 2023


<div align="center">

*Open to full-time roles in semiconductor equipment engineering, ML systems, and hardware-software co-design.*

</div>
