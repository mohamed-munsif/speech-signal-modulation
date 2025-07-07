# Speech Signal Modulation and Demodulation Project

## Overview
This project demonstrates speech signal modulation and demodulation techniques using Python. The notebook reads three audio files, resamples them to a common sampling frequency (250,000 Hz), and processes them so they all have the same length. The signals are then modulated with carrier signals and later demodulated using standard, phase-shifted, and frequency-shifted carriers.

## Features
- Audio file processing and resampling
- Signal modulation with carrier waves
- Demodulation with various carrier configurations:
  - Standard carrier
  - Phase-shifted carriers (10°, 30°, 90°)
  - Frequency-shifted carriers (2 Hz, 10 Hz)
- Signal visualization and analysis
- Audio output generation

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
└── requirements.txt       # Python dependencies
```

## Requirements
- Python 3.7+
- See `requirements.txt` for detailed dependencies

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/speech-signal-modulation.git
   cd speech-signal-modulation
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Place your audio files (.wav format) in the `signals/` folder
2. Open `project.ipynb` in Jupyter Notebook or JupyterLab
3. Run all cells to process the signals
4. Check the `output_signals/` folder for generated files

## Input Files
- **signals/**: Place your input .wav files here
  - The notebook currently processes three files: `ziad.wav`, `esoo.wav`, `mohey.wav`

## Output Files
- **output_signals/**: Contains all demodulated .wav files
  - `Out_X.wav`: Standard demodulated signals
  - `Out_X_phase_Y.wav`: Phase-shifted demodulated signals
  - `Out_X_shift_Y.wav`: Frequency-shifted demodulated signals

## Technical Details
- **Sampling Frequency**: 250,000 Hz
- **Modulation Type**: Amplitude Modulation (AM)
- **Carrier Frequencies**: Various (configurable in notebook)
- **Filter Type**: Butterworth lowpass filter for demodulation

## Dependencies
- numpy: Numerical computations
- scipy: Signal processing
- librosa: Audio processing
- soundfile: Audio file I/O
- matplotlib: Plotting and visualization
- ipython: Interactive Python environment

## License
This project is open source and available under the [MIT License](LICENSE).

## Contributing
Feel free to submit issues and enhancement requests!
