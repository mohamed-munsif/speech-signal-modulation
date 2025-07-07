# 📡 Speech Signal Modulation and Demodulation Project

<div align="center">

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Signal Processing](https://img.shields.io/badge/Signal-Processing-red.svg)
![Audio](https://img.shields.io/badge/Audio-Processing-purple.svg)

**🎵 Advanced Telecommunication System Implementation 🎵**

*A complete Python-based communication system demonstrating amplitude modulation, quadrature components, and signal recovery techniques*

**Project Partner:** [Inshaf](https://github.com/MoInshafAR)

</div>

---

## 🌟 Project Highlights

🚀 **Real-world Application**: Simulates actual telecommunication systems  
🎛️ **Multiple Modulation**: Implements AM with quadrature components  
📊 **Signal Analysis**: Complete visualization and frequency domain analysis  
🔄 **Robust Recovery**: Tests demodulation under various carrier conditions  
📱 **Easy to Use**: Interactive Jupyter notebook with step-by-step execution  

---

## � Table of Contents
- [🌟 Project Highlights](#-project-highlights)
- [📡 Overview](#-overview)
- [🔧 System Architecture](#-system-architecture)
- [📐 Mathematical Model](#-mathematical-model)
- [⚙️ Technical Specifications](#️-technical-specifications)
- [🚀 Quick Start](#-quick-start)
- [📊 Input & Output Files](#-input--output-files)
- [🛠️ Dependencies & Tools](#️-dependencies--tools)

---

## 🎬 Quick Demo

### Input → Processing → Output
```
🎤 Speech Files (ziad.wav, esoo.wav, mohey.wav)
    ↓ [Resample to 250kHz]
📡 Modulation [s(t) = x₁(t)cos(ω₁t) + x₂(t)cos(ω₂t) + x₃(t)sin(ω₂t)]
    ↓ [Transmission Simulation]
🔍 Demodulation [Standard + Phase/Frequency Shifted]
    ↓ [Low-Pass Filtering]
🎵 Recovered Audio Files (18 output variations)
```

### Results You'll Get:
- **📈 Signal Plots**: Time and frequency domain visualizations
- **🎵 Audio Files**: 18 processed audio outputs showing different recovery methods
- **📊 Analysis**: Complete comparison of demodulation techniques
- **⚡ Performance**: Real-time processing and quality assessment

---

## �📡 Overview
This project demonstrates **speech signal modulation and demodulation techniques** using Python. It implements a complete communication system that processes three audio files, modulates them using different carrier frequencies, transmits the combined signal, and then demodulates to recover the original signals.

### 🎯 Key Features
- 🎵 **Audio Processing**: Resampling and preprocessing of speech signals
- 📶 **Signal Modulation**: Amplitude modulation with quadrature components
- 🔄 **Multiple Demodulation**: Standard, phase-shifted, and frequency-shifted recovery
- 📊 **Visualization**: Complete signal analysis and plotting
- 💾 **Audio Generation**: Output of processed audio files

### 🚀 What This Project Does
1. **Input**: Reads three speech audio files (`.wav` format)
2. **Processing**: Resamples all signals to 250,000 Hz and equalizes lengths
3. **Modulation**: Combines signals using the mathematical model below
4. **Transmission**: Simulates transmission of the modulated signal
5. **Demodulation**: Recovers original signals with various carrier configurations
6. **Output**: Generates processed audio files for analysis

## 🔧 System Architecture
![Block Diagram](images/Block%20diagram.png)

**System Components:**
- **🎤 Input Stage**: Three speech signals ready for modulation
- **📡 Modulation Stage**: Signals multiplied with carrier waves
- **➕ Combiner**: All modulated signals summed to create s(t)
- **📶 Transmission**: Combined signal represents transmitted data
- **🔍 Demodulation Stage**: Signal recovery using coherent detection
- **🔽 Low-Pass Filters (L.P.F)**: Remove high-frequency components
- **🎵 Output Stage**: Recovered speech signals

### 🎛️ Demodulation Variations
- **Standard**: Perfect carrier synchronization
- **Phase-shifted**: Carriers with 10°, 30°, 90° phase offsets
- **Frequency-shifted**: Carriers with 2 Hz, 10 Hz frequency offsets

## 📐 Mathematical Model
The core of this project is based on the following modulation equation:

```
s(t) = x₁(t)cos(ω₁t) + x₂(t)cos(ω₂t) + x₃(t)sin(ω₂t)
```

**Where:**
- `s(t)` → Composite modulated signal (transmitted)
- `x₁(t), x₂(t), x₃(t)` → Input speech signals (ziad.wav, esoo.wav, mohey.wav)
- `ω₁, ω₂` → Carrier frequencies
- `cos(ω₁t), cos(ω₂t)` → Cosine carriers for signals 1 and 2
- `sin(ω₂t)` → Sine carrier for signal 3 (quadrature component)

## ⚙️ Technical Specifications
- **📡 Modulation**: Amplitude Modulation (AM) with Quadrature Components
- **🔊 Sampling Rate**: 250,000 Hz
- **🎛️ Filter Type**: Butterworth Low-Pass Filter
- **📐 Carrier Types**: Cosine and Sine waves
- **🔄 Processing**: Real-time signal visualization and analysis

## Project Structure
```
├── project.ipynb          # Main Jupyter notebook
├── signals/               # Input audio files
│   ├── esoo.wav
│   ├── mohey.wav
│   └── ziad.wav
├── output_signals/        # Generated output files
│   ├── Out_1.wav
│   ├── Out_1_phase_10.wav
│   ├── Out_1_phase_30.wav
│   ├── Out_1_phase_90.wav
│   ├── Out_1_shift_2.wav
│   ├── Out_1_shift_10.wav
│   └── ... (similar files for signals 2 and 3)
├── images/                # Documentation images
│   └── Block diagram.png
└── requirements.txt       # Python dependencies
```

## 🚀 Quick Start

### Prerequisites
- **Python 3.7+**
- **Jupyter Notebook** or **JupyterLab**

### 📥 Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/mohamed-munsif/speech-signal-modulation.git
   cd speech-signal-modulation
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

### 🎮 Usage
1. **Prepare Input**: Place your `.wav` audio files in the `signals/` folder
2. **Run Analysis**: Open `project.ipynb` and execute all cells
3. **View Results**: Check `output_signals/` for generated files
4. **Analyze**: Review plots and audio outputs

## 📊 Input & Output Files

### 📥 Input Files (`signals/` folder)
- **`ziad.wav`** → Speech signal 1 (modulated with cos(ω₁t))
- **`esoo.wav`** → Speech signal 2 (modulated with cos(ω₂t))  
- **`mohey.wav`** → Speech signal 3 (modulated with sin(ω₂t))

### 📤 Output Files (`output_signals/` folder)
- **`Out_X.wav`** → Standard demodulated signals
- **`Out_X_phase_Y.wav`** → Phase-shifted demodulated signals (Y = 10°, 30°, 90°)
- **`Out_X_shift_Y.wav`** → Frequency-shifted demodulated signals (Y = 2Hz, 10Hz)

*Where X = 1, 2, 3 corresponding to the three input signals*

## 🛠️ Dependencies & Tools

### Core Libraries
- **`numpy`** → Numerical computations and array operations
- **`scipy`** → Signal processing and filtering
- **`librosa`** → Audio processing and resampling
- **`soundfile`** → Audio file I/O operations
- **`matplotlib`** → Signal plotting and visualization
- **`ipython`** → Interactive Python environment

### Installation
All dependencies are listed in `requirements.txt` for easy installation.

## 🤝 Contributing
Feel free to submit issues and enhancement requests!

### 📞 Contact
For questions about this telecommunication project, feel free to reach out!
