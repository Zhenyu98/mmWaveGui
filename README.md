# mmWave Industrial Visualizer and Gesture Data

This repository includes the Python implementation of Texas Instruments' mmWave Industrial Visualizer along with additional assets used for gesture and posture recognition.

## Overview
The visualizer parses and displays data streamed from TI mmWave radar devices. It is designed to help evaluate and investigate different radar demos.

## Running the visualizer
After installing the required packages, the GUI can be launched directly:

```bash
python gui_main.py
```

## Requirements
The `setUpEnvironment.bat` script lists the main Python dependencies:

- pyqt5 5.15.4
- pyopengl 3.1.5
- numpy 1.19.4
- pyserial 3.5
- pyqtgraph 0.11.0
- scikit-learn 0.21.2

Install them using pip before running the program.

## Directory structure
- `gui_main.py` – main application window and plotting logic
- `gui_parser.py` – handles UART data parsing
- `gui_threads.py` – manages worker threads for I/O and graph updates
- `graphUtilities.py` – helper functions for 3D drawing
- `gui_common.py` – shared settings and constants
- `parseFrame.py` / `parseTLVs.py` – interpret the incoming frame/TLV formats
- `assets/mmWave` – scripts for processing gesture datasets
- `binData/traindata` – labelled point cloud data for actions such as static, squat, stand, tumble, etc.
- `images` – reference images for hardware setup
- `docs` – HTML copies of the official user guide and release notes

## Notes
This repo mixes official TI Visualizer code with experimental machine learning scripts and sample data. The data folders can be large. See the HTML user guide in `docs/` for more detail about running the visualizer and customizing the source.
