
<div align="center">

# **Multi Signal Viewer with AI detection**

</div>

> ## **Overview**

An integrated web-based application for **multi-domain signal visualization and analysis**, supporting **medical**, **acoustic**, and **radiofrequency** signals.
The viewer integrates multiple AI models and interactive visualization modes for real-time exploration, detection, and classification.

---

## **Included Modules**

#### 🫀 Medical Signals Viewer

- Visualize multi or single-channel `ECG/EEG` signals and detect abnormalities using a pretrained `AI model`.

#### 🔊 Acoustic Signals Viewer

- Vehicle-Passing Doppler Effect: simulate car sounds with controllable `velocity (v)` and `frequency (f)`; estimate both using an AI model from real recordings.
- Drone Detection: detect the presence of drones or submarines among background sounds using an AI classifier.

#### 📡 Radiofrequency Signals Viewer

- Visualize real `SAR` signals and estimate some features.

---
### 🏠 Home Page Preview

Here’s how the main interface of the Signal Viewer looks:

<img width="1876" height="860" alt="500076424-1053632c-122e-443c-be33-453c36f16971" src="https://github.com/user-attachments/assets/b76df7ba-cb66-47f6-84e4-bc0b49f52960" />

 

---

##  1) Medical Signals Viewer:
### Key features
- Support for multi or single-channel ECG/EEG recordings.

- Automatic abnormality detection.
- Four viewer modes:

  - `Continuous-time viewer` — scrolling viewport with navigate, zoom, and pan controls.

  - `XOR graph` — divide the signal into chunks and overlay them using XOR: identical chunks cancel out.

  - `Polar graph`

  - `Reoccurrence graph` — cumulative scatter plot of channel pairs (chx vs chy) to reveal recurring patterns.
---
## ECG demo:


https://github.com/user-attachments/assets/e8155c7f-c491-41f0-8878-0ea98ab3b1b4


### another abnormal signal: LVH 
<img width="1891" height="879" alt="2" src="https://github.com/user-attachments/assets/b1b2efeb-97a1-4344-bd22-0271dc271cd6" />

---

## EEG demo:
<img width="1882" height="913" alt="3" src="https://github.com/user-attachments/assets/ea5a0d8d-b608-4ae7-8c45-920f2141c80f" />
<img width="1893" height="883" alt="4" src="https://github.com/user-attachments/assets/87d1a54d-0b12-47c7-9c69-80d4529052e8" />

---
##  2) Acoustic Signals Viewer:
### 🚗 Doppler Effect Detection
- Uses spectrogram analysis (STFT) to track frequency changes over time and detect peaks:  
  - fₐₚₚ → approaching frequency  
  - fᵣₑc → receding frequency  
- Estimates car speed in m/s or km/h using:  
  v = c × (fₐₚₚ - fᵣₑc) / (fₐₚₚ + fᵣₑc)

  


https://github.com/user-attachments/assets/c2c5288b-508b-4743-ac9f-7100bb8362b9




---

### 🚗 Doppler Car Sound Generator

- This project simulates the Doppler effect by generating the sound of a car passing by with `velocity v` and `horn frequency f`.
- The user can control both parameters, and a spectrogram is displayed to visualize the frequency shift as the car approaches and moves away.




https://github.com/user-attachments/assets/b8e62b07-8158-4491-bd5a-cc1dc9d4eb3b



---

### Drone

This module detects drones from `WAV audio files` using `YAMNet` for feature extraction and a custom classifier, it enables users to upload audio and view predictions




https://github.com/user-attachments/assets/5763a966-4414-4542-ae5f-2692dade08b0



---
## 3)SAR
<img width="816" height="896" alt="5" src="https://github.com/user-attachments/assets/9f62939b-7d54-44ff-adac-5593bc688b0c" />

<img width="812" height="507" alt="6" src="https://github.com/user-attachments/assets/95893702-2bac-4e61-a02f-bd350b0ea62f" />


---
   
### Technologies Used

| Layer | Tools & Frameworks | Description | Data / Model Source |
|:------|:-------------------|:-------------|:--------------------|
| **Frontend** | React.js, react-plotly.js | Interactive UI for real-time signal visualization and user controls. | — |
| **Backend** | Flask (Python) | Handles signal processing, AI model inference, and data communication with the frontend. | — |
| **AI / ML Models** | TensorFlow | Pretrained models for abnormality detection (ECG/EEG), Doppler parameter estimation, and sound classification. | [ECG model](https://github.com/Edoar-do/HuBERT-ECG),  [Drone Model](https://github.com/tensorflow/models/tree/master/research/audioset/yamnet), EEG model using `CSP` and `classifier`|
| **Data Formats** | CSV | Supported formats for signal input/output. | [PhysioNet_ecg dataset](https://physionet.org/content/ptb-xl/1.0.3/), [Drones dataset](https://github.com/saraalemadi/DroneAudioDataset), [Car_sound dataset](https://slobodan.ucg.ac.me/science/vse/),EEG_dataset from brainlat |

---

## 👥 Contributors
| [Nayera Sherif](https://github.com/Nayera5) | [Nada Hesham](https://github.com/Nada-Hesham249) | [Shahd Ayman](https://github.com/Shahd-Ayman5) | [Nada Hassan](https://github.com/Nadahassan147) |
|-------------------------------|---------------------------|-----------------------------------|-------------------------------|





---
