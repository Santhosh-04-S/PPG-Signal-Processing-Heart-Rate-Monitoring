# PPG Signal Processing & Heart Rate Monitoring System

![Project Status](https://img.shields.io/badge/Status-In%20Development-blue)
![Python](https://img.shields.io/badge/Python-3.x-yellow)
![Signal Processing](https://img.shields.io/badge/Domain-Biomedical%20Signal%20Processing-green)

## Overview

The **PPG Signal Processing & Heart Rate Monitoring System** is a biomedical signal processing project developed to extract heart rate information from Photoplethysmography (PPG) signals.

The project focuses on designing a complete signal processing pipeline, starting from raw PPG signal acquisition to noise removal, heartbeat detection, and heart rate estimation.

This project demonstrates the application of **Digital Signal Processing (DSP)** techniques in wearable healthcare systems and physiological monitoring applications.

---

## Objectives

* Acquire and analyze PPG physiological signals
* Remove noise and motion artifacts using digital filters
* Detect heartbeat peaks from processed PPG signals
* Estimate heart rate in beats per minute (BPM)
* Visualize raw and processed biomedical signals
* Develop a foundation for real-time wearable heart monitoring systems

---

## System Architecture

```
                 PPG Signal Dataset
                         |
                         ↓
              Signal Loading & Visualization
                         |
                         ↓
                  Preprocessing
                         |
                         ↓
              Digital Signal Filtering
        (Bandpass Filtering + Noise Removal)
                         |
                         ↓
                 Peak Detection
                         |
                         ↓
              Heart Rate Calculation
                         |
                         ↓
             Results Visualization & Analysis
```

---

## Features

### Signal Processing

* Raw PPG signal visualization
* Baseline drift removal
* Bandpass filtering for physiological frequency range
* Noise reduction
* Signal quality analysis

### Heart Rate Estimation

* Automated heartbeat peak detection
* RR interval calculation
* Heart rate calculation in BPM
* Performance evaluation

### Visualization

* Raw PPG waveform
* Filtered PPG waveform
* Detected heartbeat peaks
* Heart rate analysis plots

---

## Technologies Used

### Programming Language

* Python

### Libraries

* NumPy
* SciPy
* Pandas
* Matplotlib
* WFDB
* HeartPy

### Concepts Applied

* Digital Signal Processing
* Biomedical Signal Analysis
* Filtering Techniques
* Peak Detection Algorithms
* Physiological Parameter Extraction

---

## Project Structure

```
PPG-Signal-Processing-Heart-Rate-Monitoring/

│
├── dataset/
│   └── raw/
│       └── PPG datasets
│
├── src/
│   ├── main.py
│   ├── load_data.py
│   ├── preprocessing.py
│   ├── filtering.py
│   ├── peak_detection.py
│   └── heart_rate.py
│
├── results/
│   ├── raw_signal.png
│   ├── filtered_signal.png
│   └── heart_rate.png
│
├── notebooks/
│   └── PPG_analysis.ipynb
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Methodology

### 1. Data Acquisition

PPG signals are obtained from publicly available physiological signal databases.

The raw signal contains information related to blood volume changes caused by cardiac activity.

---

### 2. Signal Preprocessing

The acquired PPG signal is processed to improve signal quality by reducing unwanted components such as:

* Baseline wandering
* High-frequency noise
* Motion-related artifacts

---

### 3. Digital Filtering

A bandpass filter is applied to preserve the frequency components related to human pulse activity.

Typical PPG frequency range:

```
0.5 Hz - 5 Hz
```

---

### 4. Peak Detection

Heartbeat locations are identified by detecting peaks in the filtered PPG waveform.

Detected peaks are used to calculate beat-to-beat intervals.

---

### 5. Heart Rate Calculation

Heart rate is calculated using detected peak intervals:

```
Heart Rate (BPM) = 60 / Average RR Interval
```

---

## Results

The system produces:

* Cleaned PPG waveform
* Detected heartbeat locations
* Estimated heart rate value

Example output:

```
Subject: PPG Sample

Sampling Frequency: 125 Hz

Detected Heart Beats: 72

Estimated Heart Rate: 75 BPM
```

---

## Future Improvements

Future development will include:

* Real-time PPG acquisition using MAX30102 sensor
* ESP32-based wearable monitoring device
* OLED heart rate display
* Motion artifact removal techniques
* Heart rate variability (HRV) analysis
* Machine learning based cardiovascular condition classification

---

## Applications

This project can be applied in:

* Wearable fitness devices
* Remote patient monitoring systems
* Smart healthcare devices
* Biomedical research
* Physiological signal analysis

---

## Author

**Santhosh S.**

Electronic & Telecommunication Engineering
University of Moratuwa

Interests:

* Biomedical Signal Processing
* Sensor Development
* Machine Learning Applications in Healthcare
* Embedded Systems

---

## License

This project is licensed under the MIT License.
