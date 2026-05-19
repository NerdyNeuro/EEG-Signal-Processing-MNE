# EEG-Signal-Processing-MNE
An automated end-to-end EEG processing pipeline built with MNE-Python. Features data loading/concatenation, 10-20 montage standardization, bandpass filtering, FastICA physiological artifact subtraction, time-locked epoching, and frequency-domain feature extraction (PSD). 
## 🚀 Key Features

* **Data Ingestion & Concatenation:** Seamless loading and merging of multiple contiguous European Data Format (`.edf`) files.
* **Nomenclature Standardisation:** Robust string-cleansing logic mapping physical channel configurations (e.g., trailing punctuation) dynamically to standard **International 10-20 system** templates.
* **Ocular Artifact Subtraction:** Implements Independent Component Analysis (`FastICA`) to isolate, visualize, and exclude eye blinks and motor movements.
* **Time-Locked Epoching:** Segments continuous signals into time-locked epochs centered around stimulus annotations with custom baseline correction.
* **Spectral Feature Extraction:** Computes Power Spectral Density (PSD) across standard frequency bands (Delta, Theta, Alpha, Beta).

## 🛠️ Pipeline Architecture

The pipeline enforces a logical, strict neuroscientific data workflow to preserve signal integrity:
1. **Data Loading** & Verification ➡️ 
2. **Channel Renaming** & Montage Alignment ➡️ 
3. **Bandpass Filtering** (1.0–40.0 Hz) ➡️ 
4. **Epoching & Segmentation** ➡️ 
5. **ICA Decomposition** & Artifact Removal ➡️ 
6. **Feature Extraction** (Power Spectral Density)

## 📦 Prerequisites

Ensure you have Python installed alongside the dependencies listed in `requirements.txt`:
```bash
pip install -r requirements.txt
