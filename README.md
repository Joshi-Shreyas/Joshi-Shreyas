<div align="center">

# Shreyas Joshi

**MS ECE @ Northeastern University** · Boston, MA · Graduating December 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/joshi-shreyas-ece)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:joshi.shreyas@northeastern.edu)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Joshi-Shreyas)
[![Portfolio](https://img.shields.io/badge/Portfolio-4A5568?style=flat&logo=githubpages&logoColor=white)](https://joshi-shreyas.github.io)

</div>


## About

I'm a hardware and machine learning engineer finishing my master's at Northeastern. Most of my work sits in two places: ML for semiconductor manufacturing, and GPU/HPC performance engineering.

During my co-op at Veeco Instruments in San Jose I worked with Ion Beam Deposition tools, the equipment used to lay thin films onto wafers. I built an LSTM fault detection model on the tools' multi-sensor data (AUC-PR of 0.91 on rare failure cases) and designed an I2C sensor circuit for the robotic end effector. Hardware and ML, side by side.

On the GPU side, I've been writing CUDA and Triton kernels from scratch, benchmarking them against cuBLAS, and taking apart where time actually goes in distributed PyTorch training. The work I like most is where you have to understand both what the machine is physically doing and what the model actually needs.


## Selected Projects

### Semiconductor Process & Manufacturing ML

| Project | What it does | Stack |
|---|---|---|
| [DRAM Capacitor DOE, SPC & AI-Assisted Root-Cause Analysis](https://github.com/Joshi-Shreyas/dram-capacitor-doe-spc) | Simulated a DRAM MIM capacitor process end to end: a physics-grounded model of capacitance, leakage, and reliability tradeoffs, a CCD Design of Experiments with RSM to find the optimal recipe, SPC monitoring of simulated production, and a Mahalanobis multivariate detector that catches excursions univariate charts miss (false alarms 5.7% to 1.4%). An LLM pipeline drafts root-cause investigation reports, with its failure modes documented. | Python · pyDOE3 · statsmodels · SciPy · pandas · Matplotlib · Gemini API |
| [Plasma Etch Bayesian Optimization](https://github.com/Joshi-Shreyas/plasma-etch-bayesian-optimization) | GP based Bayesian optimization for etch recipe targeting across a 4D parameter space. Mean deviation of 0.81 ± 0.55 Å/min from target over 65 experiments, beating factorial DOE and random search baselines. Multi objective Pareto front via qLogNEHVI. | BoTorch · GPyTorch · PyTorch · Python |
| [Plasma Etch Surrogate Model](https://github.com/Joshi-Shreyas/plasma-surrogate) | Neural network digital twin that predicts plasma etch rate across 300mm wafers. 94.19% accuracy, sub millisecond inference, roughly 1000x faster than the physical solver. Trained on Northeastern's HPC cluster. | PyTorch · NumPy · Matplotlib · Slurm |
| [Wafer Defect Open-Set Rejection](https://github.com/Joshi-Shreyas/wafer-defect-open-set-rejection) | Open-set defect classification on WM811K wafer maps, so the model flags defect types it has never seen instead of forcing a wrong label. Compared supervised ResNet-18 with MAE self-supervised features; Mahalanobis scoring lifted unknown-defect AUROC from 0.50 to 0.997. A cost-sensitive rejection framework cut estimated operational cost by 32 to 42%. | PyTorch · ResNet-18 · MAE · scikit-learn · Slurm |

### GPU & HPC Systems

| Project | What it does | Stack |
|---|---|---|
| [CUDA Tiled Matmul + PyTorch Extension](https://github.com/Joshi-Shreyas/cuda-tiled-matmul-pytorch) | Tiled matrix multiply kernel with shared-memory blocking, exposed to PyTorch as a custom C++/CUDA extension and benchmarked against cuBLAS on a V100 (about 4.2x slower, with the gap broken down). Rebuilt in Triton (about 1.37x of cuBLAS) and added autotuning over 5 configs for another ~5%. Roofline analysis predicted a 16x memory traffic reduction from tiling; measured 1.7x, traced to L2 cache effects. | CUDA C++ · Triton · PyTorch C++ Extensions · pybind11 · cuBLAS · V100 |
| [DDP Scaling Analysis](https://github.com/Joshi-Shreyas/ddp-scaling-analysis) | Decomposed per-step PyTorch DDP training time into compute, all-reduce, and I/O on V100s over NVLink. NCCL vs Gloo comparison (30x bandwidth gap), bucket-size sweeps to measure how much communication hides behind compute, and a demonstration that all-reduce cost stays flat as batch size grows. | PyTorch DDP · NCCL · Gloo · CUDA Events · Slurm · NVLink |
| [CUDA & MPI Parallel Performance](https://github.com/Joshi-Shreyas/cuda-parallel-performance-analysis) | Coalesced vs non coalesced CUDA kernel benchmarks on a Tesla V100 (5.8x speedup, 640 GB/s peak bandwidth), plus distributed MPI histogramming across one and two HPC nodes, with bottleneck isolation through MPI_Scatterv analysis. | CUDA C · OpenMPI · C · Slurm |
| Parallel Image Segmentation (CPU) | K-means segmentation with OpenMP and SSE4.2 SIMD. 10.78x speedup, 86.9% energy savings. Extended Amdahl's Law with a 2D parallelism model that cut prediction error from the 41 to 52 percent range down to under 8 percent. | C · OpenMP · SIMD · Intel VTune · Roofline |

### Edge AI & Model Efficiency

| Project | What it does | Stack |
|---|---|---|
| [LingBot-VA: Vision Action Robot Control](https://github.com/Joshi-Shreyas/Lingbot-va-int8-Quantization) | INT8 quantization of a vision action transformer for robot manipulation. 49% lower inference latency, 17.2% less VRAM, and task success up from 43.8% to 87.5% on the open_microwave benchmark. Evaluated on A100 GPUs. | PyTorch · INT8 Quantization · A100 |
| [Voice Interaction System](https://github.com/Joshi-Shreyas/voice-interaction-system) | Voice assistant and speech-to-speech translator that runs fully on local hardware, no cloud, at 2.96s end to end. Quantized Qwen2.5-7B through llama.cpp for the language model, Whisper-medium for speech to text, and Kokoro-82M / F5-TTS for text to speech. | llama.cpp · Whisper · Kokoro · F5-TTS · Python |
| Continual Learning on ImageNet *(in progress)* | Class incremental learning with iCaRL on a ResNet50 backbone, looking at how to add new ImageNet classes over time without catastrophic forgetting. | PyTorch · iCaRL · ResNet50 |

### Security

| Project | What it does | Stack |
|---|---|---|
| Secure ECC Communication | Hybrid ECDH and AES-256 encryption with ECDSA authentication. Caught 100% of simulated interception (MITM) attacks. Machine learning anomaly detection on signatures. | Python · ECC · AES-256 |


## Experience

**Veeco Instruments** · Electrical Engineer Co-op, R&D · San Jose, CA · *Jul to Dec 2025*

- Built a hybrid LSTM fault detection model on multi-sensor time series data from Ion Beam Deposition tools, using synthetic data augmentation for rare fault classes, reaching AUC-PR of 0.91.
- Designed an I2C based sensor interfacing circuit for a robotic end effector.

**Northeastern University** · Teaching Assistant · *Jan 2025 to Present*

- Digital Design & Computer Architecture (EECE 2310). Promoted from Lab TA to Course and Lab TA. Verilog and FPGA work on the DE1-SoC with Quartus Prime. Walked students through ALUs, binary adders, counters, and timing analysis and simulation.
- Analysis of Random Phenomena (EECE 3468), May to Present.

**IEEE CASS Bangalore Chapter** · Student Intern · *Oct to Dec 2023*

- Implemented CRC-16 error detection in Verilog using an LFSR. Took 2nd Runner-Up for Best Internship Presentation across Karnataka State.

**Renalyx Health Systems** · Hardware Intern · Bangalore, India · *Dec 2022 to Jan 2023*

- PCB design and validation in OrCAD, embedded firmware for Renesas MCUs in E2 Studio, and signal conditioning and power management for biomedical sensors. Worked on hardware validation for a dialysis machine in a regulated medical device environment, including BOM generation and ECO documentation.

**BHT Technologies** · Product Development Intern · *Oct to Dec 2022*

- Embedded work on Arduino, ESP32, ESP32-CAM, and Teensy. Wireless over Wi-Fi, BLE, and MQTT. IoT sensor interfacing with live data transmission, programmed in C/C++ and Python.


## Tech Stack

```
ML & AI             PyTorch · TensorFlow · Scikit-learn · BoTorch · GPyTorch · NumPy · SciPy · OpenCV
Edge AI             llama.cpp · Whisper · Kokoro TTS · INT8 Quantization
GPU Programming     CUDA C/C++ · Triton · cuBLAS · PyTorch C++ Extensions · pybind11 · Roofline
Distributed & HPC   PyTorch DDP · NCCL · OpenMPI · OpenMP · SIMD/SSE · Slurm · Intel VTune
Process & Stats     DOE (CCD, RSM) · SPC · CpK · JMP · pyDOE3 · statsmodels
Systems             x86 · RISC-V · ARM · FPGA (Quartus, Xilinx) · Verilog · VHDL · Linux
Embedded            Arduino · ESP32 · Teensy · I2C · SPI · UART · BLE · MQTT
EDA & Tools         Cadence Allegro · OrCAD · PSpice · ModelSim · SolidWorks
Languages           Python · C/C++ · CUDA C · Java · MATLAB · Bash
```

**Domains**

```
Semiconductor       Thin Film Deposition (IBD) · Plasma Etch · DRAM Capacitor Process · Wafer Defect Analysis
Manufacturing ML    Fault Detection · Predictive Maintenance · Digital Twins · Open-Set Classification
GPU Systems         Kernel Optimization · Distributed Training · Collective Communication · Performance Modeling
Edge AI             Model Quantization · On-Device Inference · Speech Pipelines
```


## Education

**Northeastern University, Boston** · MS Electrical & Computer Engineering · GPA 3.73 · Dec 2026
Concentration: Computer Systems and Software
*Coursework: Deep Learning Embedded Systems, Machine Learning and Pattern Recognition, High Performance Computing, Thin Film Technology (in progress), Computer Architecture, Hardware Security, Data Visualization*

**Bangalore Institute of Technology** · B.E. Electronics & Communication Engineering · GPA 8.89/10 · May 2024


## Publications

- **"A High Speed Memristor Digital Quadrature Clock Generation"**, Patent and Design Journal India, June 2023


<div align="center">

*Open to full-time roles in semiconductor equipment and process engineering, manufacturing ML, and GPU/HPC systems.*

</div>
