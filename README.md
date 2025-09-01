

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
```
Cutie is automatically cloned and configured inside the notebook.

## 🎬 Usage

### Upload your video to Colab or Google Drive

**Update the path in the notebook:**

video_path = "/content/drive/MyDrive/your-video.mp4"

**Set your detection text query:**

text_queries = [["basketball", "ball"]]

Run the pipeline → It will:

Detect objects (OWLv2)

Segment them (SAM2)

Track across frames (Cutie)

Save output video: output/tracked_video.mp4
## System Architecture Flow

<img width="284" height="820" alt="Arch Flow" src="https://github.com/user-attachments/assets/9b6a93b8-d011-4fda-ad38-8c6e9531adea" /># Object-Tracking-Pipeline

## 🛠️ How It Works
1️⃣ **OWLv2 — Open-World Object Detection**

Developed by Google

Detects objects by text query (e.g., "car", "dog")

Works with any natural language object

Unlike YOLO or Faster R-CNN, no fixed label set

2️⃣ **SAM2 — Segment Anything Model v2**

Developed by Meta AI

Generates pixel-perfect masks from bounding boxes

Example: OWLv2 detects a rectangle → SAM2 refines into the exact object shape

3️⃣ **Cutie — Tracking Across Frames**

Maintains object identity across video frames

Handles occlusion, fast motion, and reappearance

Combines with OWLv2 + SAM2 to produce smooth, consistent tracked video

## 📺 Example Results
**Original Frame from Video**

<img width="415" height="310" alt="Original_Frame_from_Video" src="https://github.com/user-attachments/assets/d6041175-efa5-4cb4-a5c4-5b8e8022573e" />

**OWLv2 + SAM2 Detection + Segmentation**

<img width="1233" height="488" alt="OWLV2+SAM2 Output" src="https://github.com/user-attachments/assets/1816e4e7-cf65-424c-8893-c8fee25325d2" />

**Cutie Tracking Result**

<img width="1333" height="486" alt="first_frame_output" src="https://github.com/user-attachments/assets/fd5c7601-5a5a-4cd7-b965-c4304c05d7e5" />

<img width="1357" height="498" alt="Last_Frame_Output" src="https://github.com/user-attachments/assets/1f1f6e19-b2ca-4cd5-8e35-e07c41c021f2" />

## 🎥 Videos
Original Video

<video src="output/original_video.mp4" width="600" controls></video>

## Tracked Output Video

<video src="output/tracked_video.mp4" width="600" controls></video>

If the video doesn’t play inline, click the file in the output/ folder to download and watch.

## 📋 Summary

✅ Detect objects using text queries (OWLv2)
✅ Segment precisely (SAM2)
✅ Track objects through video (Cutie)
✅ Save video and frames for reporting

💡 Try changing text_queries in the notebook to track different objects!
