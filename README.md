# mmWave SAR Defect Detection System

**This mmWave SAR imaging system was developed as a collaborative research project between Inha University (South Korea) and University of Southern California (USA).**

> Part of collaborative research published in IEEE Access 2025
> DOI: [10.1109/ACCESS.2025.3531913]

## Project Context

Internal defect detection in manufacturing requires expensive, slow equipment. This project demonstrates a using mmWave radar achieving **91.7% accuracy**.

![alt text](<hardware/radar_control/photos/Overview of a complete mmWave imaging system.png>)
![alt text](<hardware/mmWave scanning & acquisition.png>)


**This repository showcases my contributions** to the **hardware**, **signal processing**, and **image reconstruction** components of the complete system.

## My Contributions (Inha)

### 1. **Compact mmWave Radar System Design**

Designed and built a portable scanning platform integrating:

- Texas Instruments AWR1843 FMCW radar (77-81 GHz, 4 GHz bandwidth)
- DCA1000 high-speed data acquisition module
- Dual-rail motorized scanning platform (200×200mm aperture)
  - **Real-time synchronization** between motor position and radar chirps
  - **Precision positioning**: 0.8mm step size (sub-wavelength sampling)
  - **Speed**: 20 mm/s with minimal vibration noise

📁 **Code**: `/hardware/radar_control/`, `/hardware/data_acquisition/`, `/hardware/motion_control/`

### 2. **SAR Image Reconstruction**

Implemented **Range Migration Algorithm** for near-field SAR imaging:

- FMCW signal processing and range-FFT
- Matched filtering for focused image formation
- Near-field approximations for sub-wavelength resolution

📁 **Code**: `/signal_processing/sar_reconstruction/`

### 3. **DTCWT Denoising for Near-Field SAR Images**

Developed and validated wavelet-based noise reduction algorithm:

- Implemented **Dual-Tree Complex Wavelet Transform** with real/imaginary filter branches
- **Performance**: Improved PSNR by 8-12 dB across test distances.

📁 **Code**: `/signal_processing/wavelet_denoising/`

## Collaborative Components

### Defect Detection Algorithm (USC Team)

The automated defect localization using Process-Informed Smooth Sparse
Decomposition (PISSD) was developed by **Weizhi Lin and Qiang Huang**
at University of Southern California.

**My role**: Provided SAR images and experimental data; collaborated on
algorithm validation.

**Their algorithm**: Decomposed images into background/defect/noise
components using domain-informed basis functions.

For details on PISSD implementation, see the published paper or contact
the USC team.

## Collaboration Model

This project demonstrates hardware-software co-design:

- **Inha (Hardware)**: Built the physical scanning system and preprocessing
- **USC (Software)**: Developed the automated detection algorithms
- **Joint**: Experimental validation and paper writing

## Technical Skills Demonstrated

### Hardware Engineering

- mmWave radar system integration
- Motorized scanning platform design

### Signal Processing

- FMCW radar signal processing
- SAR image reconstruction algorithms
- Wavelet transform implementation
