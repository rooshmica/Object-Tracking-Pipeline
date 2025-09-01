# Object-Tracking-Pipeline

# 🎯 Complete OWLv2 + SAM2 + Cutie Object Tracking Pipeline

This repository contains a **step-by-step Colab tutorial** for building a powerful **object tracking pipeline** using:

- **OWLv2** – Text-based object detection  
- **SAM2** – Pixel-perfect segmentation  
- **Cutie** – Robust object tracking across frames  

## 🚀 Features
- Detect **any object** by text description (no training needed!)
- Generate **precise segmentation masks**
- Track objects seamlessly across video frames
- Works with **people, cars, animals, sports equipment**, and more
- Handles **occlusion, fast movement, and complex scenes**

## 📦 Installation
Run the following inside Google Colab:

```bash
!pip install -q transformers timm torchvision huggingface_hub pillow opencv-python matplotlib
!pip install -q git+https://github.com/facebookresearch/sam2.git
Cutie setup is handled automatically in the notebook.

