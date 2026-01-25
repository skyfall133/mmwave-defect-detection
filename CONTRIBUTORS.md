# Contributors

## Project Overview

This mmWave SAR imaging system was developed as a collaborative research project between Inha University (South Korea) and University of Southern California (USA).

## Published Paper

Bui, Q.C., Lin, W., Huang, Q., & Byun, G.S. (2025). Automated Internal
Defect Identification and Localization Based on a Near-Field SAR
Millimeter-Wave Imaging System. IEEE Access.
DOI: 10.1109/ACCESS.2025.3531913

## Contribution Breakdown

### Quoc Cuong Bui & Gyun Su Byun (Inha University)

**Hardware & Signal Processing**

- Built hardware integration for TI AWR1843BOOST + DCA1000EVM
- Developed stabilized dual-rail scanning mechanism with motion control
- Contributed to SAR image reconstruction using Range Migration Algorithm
- Implemented DTCWT-based denoising algorithm for near-field SAR images
- Conducted all experimental testing with 3D-printed samples

**Code in this repository**:

- `/hardware/*` - Complete hardware design and implementation
- `/radar_control/*` - Scanning platform control and synchronization
- `/signal_processing/wavelet_denoising/*` - DTCWT filter implementation
- `/signal_processing/sar_reconstruction/*` - SAR imaging algorithms

### Weizhi Lin & Qiang Huang (USC)

**Algorithm Development**

- Developed Process-Informed Smooth Sparse Decomposition (PISSD) algorithm
- Created automated defect localization method
- Designed basis functions for image decomposition
- Implemented grid search optimization for hyperparameters

**Note**: The defect detection algorithm code is maintained separately by
the USC team. For inquiries about PISSD implementation, please contact
the USC collaborators.

## Collaboration Model

This project demonstrates hardware-software co-design:

- **Inha (Hardware)**: Built the physical scanning system and preprocessing
- **USC (Software)**: Developed the automated detection algorithms
- **Joint**: Experimental validation and paper writing
