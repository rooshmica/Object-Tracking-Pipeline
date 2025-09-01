# Object-Tracking-Pipeline

# 🎯 Complete OWLv2 + SAM2 + Cutie Object Tracking Pipeline

This repository demonstrates a **step-by-step Colab tutorial** for building a **powerful object tracking pipeline** combining:

- **OWLv2** → Detect objects just by describing them in text  
- **SAM2** → Generate pixel-perfect segmentation masks  
- **Cutie** → Track detected objects across video frames  

---

## 🚀 Features
- Detect **any object** (person, car, dog, ball, etc.) by simple text queries
- Create **precise segmentation masks** using SAM2
- Track objects smoothly with Cutie, even in **occlusion** or **fast motion**
- Works on any video you provide

---

## 📦 Installation
Run inside **Google Colab**:

```bash
!pip install -q transformers timm torchvision huggingface_hub pillow opencv-python matplotlib
!pip install -q git+https://github.com/facebookresearch/sam2.git
