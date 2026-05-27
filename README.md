<div align="center">

# Shreyas Joshi

**MS ECE @ Northeastern University** · Boston, MA · Graduating Dec 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/b71683240)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:joshi.shreyas@northeastern.edu)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Joshi-Shreyas)

</div>


## About Me

I work at the intersection of **hardware systems and machine learning** — building things that run close to silicon and think with data. My background spans semiconductor equipment engineering, embedded firmware, HPC-scale ML, and computer architecture.

Most recently at **Veeco Instruments** (San Jose), I built hybrid LSTM models for early fault detection on Ion Beam Deposition systems, achieving AUC-PR of 0.91 on rare fault classes. I also designed sensor interfacing circuits for robotic end-effector calibration — hardware and ML, not one or the other.

I think about problems from both ends: what the silicon is doing, and what the model needs to learn.


## Selected Projects

| Project | What it does | Stack |
|---|---|---|
| [Plasma Etch Surrogate Model](https://github.com/Joshi-Shreyas/plasma-surrogate) | Neural network digital twin for plasma etch rate prediction across 300mm wafers. 97.6% accuracy, sub-millisecond inference, 1000x speedup over physical solvers. Trained on Northeastern HPC (SLURM). | PyTorch · NumPy · Matplotlib · SLURM |
| LingBot-VA: Vision-Action Robot Control | INT8 quantization of a vision-action transformer for robot manipulation. 49% inference speedup, 17.2% VRAM reduction, 43.8%→87.5% task success on open_microwave benchmark. Evaluated on A100 GPUs. | PyTorch · INT8 Quantization · A100 HPC |
| Parallel Image Segmentation (CPU+GPU) | K-means segmentation with OpenMP + SSE4.2 SIMD. 10.78× speedup, 86.9% energy savings. Identified super-linear speedup via cache threshold analysis. Extended Amdahl's Law with 2D parallelism model. | C · OpenMP · SIMD · Intel VTune · Roofline |
| Secure ECC Communication | Hybrid ECDH + AES-256 encryption with ECDSA authentication. 100% MITM attack detection. ML-based signature anomaly detection. | Python · ECC · AES-256 |
| Epileptic Seizure Detection | DWT feature extraction on EEG biomedical data. SVM achieved 98% accuracy across benchmarked classifiers. | Python · MATLAB · SVM · DWT |


## Experience Highlights

**Veeco Instruments** · Electrical Engineer Co-op · *Jul–Dec 2025*
> Hybrid LSTM for fault detection on IBD semiconductor systems (AUC-PR 0.91) · Multi-sensor data acquisition pipelines · I2C sensor interfacing for robotic calibration · Equipment diagnostics and validation

**Northeastern University** · Teaching Assistant, Digital Design & Computer Architecture · *Jan 2025–Present*
> Verilog · FPGA (DE1-SoC, Quartus Prime) · Computer Architecture · Promoted from Lab TA to Course + Lab TA

**IEEE CASS Bangalore Chapter** · Student Intern · *Oct–Dec 2023*
> CRC-16 error detection in Verilog using LFSR · 2nd Runner-Up, Best Internship Presentation across Karnataka State


## Tech Stack

```
ML & AI         PyTorch · TensorFlow · Scikit-learn · NumPy · SciPy · OpenCV · INT8 Quantization
Systems         x86 · RISC-V · ARM · FPGA (Quartus, Xilinx) · Verilog · VHDL · Linux
HPC             SLURM · OpenMP · SIMD/SSE · MPI · Intel VTune · Roofline Analysis · CUDA
Embedded        Arduino · ESP32 · Teensy · I2C · SPI · UART · BLE · MQTT
EDA & Tools     Cadence Allegro · OrCAD · PSpice · ModelSim · SolidWorks
Languages       Python · C/C++ · Java · MATLAB · Bash
Domain          Semiconductor Manufacturing · Plasma Etch · Digital Twins · Predictive Maintenance
```


## Education

**Northeastern University, Boston** · MS Electrical & Computer Engineering · GPA 3.6 · Dec 2026
Concentration: Computer Systems and Software
*Coursework: Deep Learning, HPC, Computer Architecture, Hardware Security, Embedded Systems*

**Bangalore Institute of Technology** · B.E. Electronics & Communication Engineering · GPA 8.89/10 · May 2024


## Publications

- **"A High Speed Memristor Digital Quadrature Clock Generation"** — Patent and Design Journal India, June 2023


<div align="center">

*Open to full-time roles in semiconductor equipment engineering, ML systems, and hardware-software co-design.*

</div>
