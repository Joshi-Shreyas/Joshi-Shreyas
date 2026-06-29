<div align="center">

# Shreyas Joshi

**MS ECE @ Northeastern University** · Boston, MA · Graduating December 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/joshi-shreyas-ece)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:joshi.shreyas@northeastern.edu)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/Joshi-Shreyas)

</div>


## About

I'm a hardware and machine learning engineer finishing my master's at Northeastern. Most of my experience sits in semiconductor equipment, predictive maintenance models, and GPU/HPC performance work.

During my co-op at Veeco Instruments in San Jose I worked on Ion Beam Deposition tools, the equipment used to lay thin films onto wafers in chip manufacturing. I built LSTM models that catch faults early (AUC-PR of 0.91 on the rare failure cases) and designed the sensor circuits used to calibrate the robotic end effectors on those tools. Hardware and ML, side by side.

Lately a lot of my time goes into inference efficiency: quantizing models, running LLMs on local hardware, and squeezing more out of CUDA kernels. The work I like most is where you have to understand both what the machine is physically doing and what data the model actually needs to be useful.


## Selected Projects

| Project | What it does | Stack |
|---|---|---|
| [Plasma Etch Bayesian Optimization](https://github.com/Joshi-Shreyas/plasma-etch-bayesian-optimization) | GP based Bayesian optimization for semiconductor etch recipe targeting across a 4D parameter space. Mean deviation of 0.81 ± 0.55 Å/min from target, beating factorial DOE and random search baselines. Multi objective Pareto front via qLogNEHVI. | BoTorch · GPyTorch · PyTorch · Python |
| [Plasma Etch Surrogate Model](https://github.com/Joshi-Shreyas/plasma-surrogate) | Neural network digital twin that predicts plasma etch rate across 300mm wafers. 94.19% accuracy, sub millisecond inference, roughly 1000x faster than the physical solver. Trained on Northeastern's HPC cluster. | PyTorch · NumPy · Matplotlib · Slurm |
| [CUDA & MPI Parallel Performance](https://github.com/Joshi-Shreyas/cuda-parallel-performance-analysis) | Coalesced vs non coalesced CUDA kernel benchmarks on a Tesla V100 (5.8x speedup, 640 GB/s peak bandwidth), plus distributed MPI histogramming across one and two HPC nodes, with bottleneck isolation through MPI_Scatterv analysis. | CUDA C · OpenMPI · C · Slurm |
| [LingBot-VA: Vision Action Robot Control](https://github.com/Joshi-Shreyas/Lingbot-va-int8-Quantization)  | INT8 quantization of a vision action transformer for robot manipulation. 49% lower inference latency, 17.2% less VRAM, and task success up from 43.8% to 87.5% on the open_microwave benchmark. Evaluated on A100 GPUs. | PyTorch · INT8 Quantization · A100 |
| [Voice Interaction System] (https://github.com/Joshi-Shreyas/voice-interaction-system) | A voice assistant that runs fully on local hardware, no cloud. Qwen2.5-7B served through llama.cpp for the language model, Whisper-medium for speech to text, and Kokoro-82M for text to speech. | llama.cpp · Whisper · Kokoro · Python |
| Parallel Image Segmentation (CPU and GPU) | K-means segmentation with OpenMP and SSE4.2 SIMD. 10.78x speedup, 86.9% energy savings. Extended Amdahl's Law with a 2D parallelism model that cut prediction error from the 41 to 52 percent range down to under 8 percent. | C · OpenMP · SIMD · Intel VTune · Roofline |
| Continual Learning on ImageNet *(in progress)* | Class incremental learning with iCaRL on a ResNet50 backbone, looking at how to add new ImageNet classes over time without catastrophic forgetting. | PyTorch · iCaRL · ResNet50 |
| Secure ECC Communication | Hybrid ECDH and AES-256 encryption with ECDSA authentication. Caught 100% of simulated interception (MITM) attacks. Machine learning anomaly detection on signatures. | Python · ECC · AES-256 |


## Experience

**Veeco Instruments** · Electrical Engineer Co-op · *Jul to Dec 2025*

- Built a hybrid LSTM model on time series data from multiple IBD sensors, with class balancing, reaching AUC-PR of 0.91 on rare fault detection.
- Built the data acquisition and preprocessing pipelines that fed hardware diagnostics into the ML side for predictive maintenance.
- Designed an I2C based sensor interfacing circuit for robotic end effector calibration.
- Ran diagnostics, calibration, and validation on IBD process equipment, and supported electrical design reviews and hardware specification documentation.

**Northeastern University** · Teaching Assistant · *Jan 2025 to Present*

- Digital Design & Computer Architecture (EECE 2310). Promoted from Lab TA to Course and Lab TA. Verilog and FPGA work on the DE1-SoC with Quartus Prime. Walked students through ALUs, binary adders, counters, and timing analysis and simulation.
- Analysis of Random Phenomena (EECE 3468), May to Present.

**IEEE CASS Bangalore Chapter** · Student Intern · *Oct to Dec 2023*

- Implemented CRC-16 error detection in Verilog using an LFSR. Took 2nd Runner-Up for Best Internship Presentation across Karnataka State.

**Renalyx Health Systems** · Hardware Intern · *Dec 2022 to Jan 2023*

- PCB design and validation in OrCAD, embedded firmware for Renesas MCUs in E2 Studio, and signal conditioning and power management for biomedical sensors. Worked on hardware validation for a dialysis machine in a regulated medical device environment, including BOM generation and ECO documentation.

**BHT Technologies** · Product Development Intern · *Oct to Dec 2022*

- Embedded work on Arduino, ESP32, ESP32-CAM, and Teensy. Wireless over Wi-Fi, BLE, and MQTT. IoT sensor interfacing with live data transmission, programmed in C/C++ and Python.


## Tech Stack

```
ML & AI         PyTorch · TensorFlow · Scikit-learn · BoTorch · GPyTorch · NumPy · SciPy · OpenCV
Edge AI         llama.cpp · Whisper · Kokoro TTS · INT8 Quantization
GPU & HPC       CUDA · OpenMPI · OpenMP · SIMD/SSE · Slurm · Intel VTune · Roofline
Systems         x86 · RISC-V · ARM · FPGA (Quartus, Xilinx) · Verilog · VHDL · Linux
Embedded        Arduino · ESP32 · Teensy · I2C · SPI · UART · BLE · MQTT
EDA & Tools     Cadence Allegro · OrCAD · PSpice · ModelSim · SolidWorks
Languages       Python · C/C++ · CUDA C · Java · MATLAB · Bash
Domain          Semiconductor Equipment · Plasma Etch · Digital Twins · Predictive Maintenance
```


## Education

**Northeastern University, Boston** · MS Electrical & Computer Engineering · GPA 3.73 · Dec 2026
Concentration: Computer Systems and Software
*Coursework: Deep Learning, Embedded Systems, Machine Learning, High Performance Computing, Computer Architecture, Hardware Security, Data Visualization*

**Bangalore Institute of Technology** · B.E. Electronics & Communication Engineering · GPA 8.89/10 · May 2024


## Publications

- **"A High Speed Memristor Digital Quadrature Clock Generation"**, Patent and Design Journal India, June 2023


<div align="center">

*Open to full-time roles in semiconductor equipment, ML systems, and hardware and software co-design.*

</div>
