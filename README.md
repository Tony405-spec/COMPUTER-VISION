## **`Team players`**
### Team head - Tony405-spec
### Team member - Kate020-cpu
### Team member - Jammie Mwendwa

Project Players
Project head - Tony405-spec
Team member - Kate020-cpu

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=26&pause=600&color=FF0000&center=true&vCenter=true&width=1500&lines=[!]_-_VISION_CORE_INJECTION_DETECTED;>>>_WAKING_NEON_NETS_>>>_[░░░░░░░░░░]_0%25;>>>_LOADING_CV_KERNEL_[████▓░░░░░]_45%25_::_OpenCV_4.8.0;>>>_IGNITING_RESNET152_[███████▓░░]_75%25_::_Deep_Residual_Fire;>>>_LOCKING_YOLOv11_[████████▓░]_90%25_::_Real-Time_Hunter;>>>_FUSING_ENSEMBLE_BLADE_[██████████]_100%25_::_Quantum_Cut;✓✓✓_SYSTEM_ARMED_·_DEPLOY_IMMINENT_✓✓✓" alt="Neon Typing Boot" />
</p>

<br>

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-ONLINE-red?style=for-the-badge&logo=github&logoColor=white&labelColor=black&color=ff0000"/>
  <img src="https://img.shields.io/badge/MODE-AGGRESSIVE-red?style=for-the-badge&logo=stackblitz&logoColor=white&labelColor=black&color=ff0000"/>
  <img src="https://img.shields.io/badge/ACCURACY-94%25-brightgreen?style=for-the-badge&logo=accuracy&logoColor=white&labelColor=black&color=green"/>
</p>

<br>

# **`Live Demo`**
<p align="center">
  <img src="assets/cv-demo.gif" alt="Computer Vision Demo in Action" width="90%">
</p>

---

## What is this?

**A real-time object detection & classification system** built for edge deployment. This project fuses **YOLOv11**, **ResNet152**, and **OpenCV** to detect and classify objects in video streams with **94% mAP** at 30+ FPS on a standard GPU.

**Use cases:** Surveillance analytics, retail foot traffic counting, autonomous navigation prototypes.

---

##  Core Capabilities

| Capability | Implementation |
|------------|----------------|
| Object Detection | YOLOv11 (custom‑tuned) |
| Image Classification | ResNet152 ensemble |
| Real‑Time Inference | OpenCV + CUDA acceleration |
| Supported Classes | 80 (COCO) + 5 custom (fire, weapon, etc.) |
| Frame Rate | 30–45 FPS on RTX 3060 |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.8.0-red?logo=opencv)
![YOLO](https://img.shields.io/badge/YOLOv11-ultralytics-purple)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange?logo=pytorch)
![CUDA](https://img.shields.io/badge/CUDA-11.7-green?logo=nvidia)


---

##  Project Structure
COMPUTER-VISION/
├── assets/
│ └── cv-demo.gif
├── models/
│ ├── yolov11-custom.pt
│ └── resnet152.pth
├── src/
│ ├── detect.py
│ ├── classify.py
│ └── utils.py
├── requirements.txt
├── demo.ipynb
└── README.md

---

##  Quick Start

```bash
# Clone the repo
git clone https://github.com/Tony405-spec/COMPUTER-VISION.git
cd COMPUTER-VISION

# Install dependencies
pip install -r requirements.txt

# Run detection on a test image
python src/detect.py --source assets/sample.jpg

# Run real‑time webcam detection
python src/detect.py --source 0 --conf 0.5
