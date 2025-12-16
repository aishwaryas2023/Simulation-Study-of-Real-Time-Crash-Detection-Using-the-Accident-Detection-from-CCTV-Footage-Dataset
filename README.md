# Real-Time Crash Detection and Alert System

This project detects accidents in real-time from CCTV footage using a ResNet50-based CNN and simulates post-accident alert transmission in MATLAB. Alerts are sent reliably using adaptive modulation and unequal error protection.

---

## Features
- Real-time accident detection from CCTV frames  
- Post-accident alert simulation via MATLAB  
- Reliable multi-channel alert transmission (SMS, dashboard)  
- End-to-end workflow: video → CNN detection → alert simulation  

---

## Dataset
- **Source:** Accident Detection from CCTV Footage (Kaggle)  
- **Total images:** 1,528  
  - Training: 1,006  
  - Validation: 483  
  - Testing: 39  
- Preprocessing: resized to 224×224, normalized, manually selected clear frames  
- Data augmentation: horizontal flip, small-angle rotation, color jitter, random cropping  

---

## Methodology
1. **Accident Detection**
   - ResNet50 CNN (transfer learning)  
   - Trained for 35 epochs, batch size 16, GPU-accelerated  
   - Validation Accuracy: 94.9%  
   - Precision, Recall, F1-score: ~93%  

2. **Post-Accident Alert Simulation**
   - MATLAB module simulates alert sending  
   - Uses adaptive modulation and unequal error protection (UEP)  
   - High-priority alerts delivered reliably even in noisy conditions  

3. **Workflow**
   1. Upload CCTV video → extract frames  
   2. Classify frames as accident/non-accident  
   3. Trigger MATLAB alert simulation  
   4. Check reliability of message delivery  

---

## Results
- Accurate accident detection (TP=43, TN=48, FP=4, FN=3)  
- Robust alert transmission under noisy channels  
- Demonstrates end-to-end accident detection and alerting system  

---

## Tools & Technologies
- **Deep Learning:** ResNet50, CNN  
- **Programming:** Python, MATLAB  
- **Libraries:** OpenCV, PyTorch/Keras  
- **Platform:** Google Colab (GPU)  

---

## Authors
- Bojja Divya 
- Swetha CA
- Aishwarya S
  
---
## License
This repository documents the project methodology. **Source code is not included** due to collaboration constraints.
