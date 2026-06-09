
# 🌱 Weed Detection using YOLOv8

<div align="center">

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge\&logo=python)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-red?style=for-the-badge)
![PyTorch](https://img.shields.io/badge/PyTorch-2.1-orange?style=for-the-badge\&logo=pytorch)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-Object%20Detection-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### 🚜 Deep Learning for Precision Agriculture

Detecting weeds in agricultural fields using the YOLOv8 object detection framework.

</div>

---

## 📌 Project Overview

Weed infestation is one of the major challenges affecting crop productivity worldwide. Manual weed monitoring is labor-intensive and time-consuming.

This project develops a **YOLOv8-based object detection model** capable of automatically identifying weeds from agricultural imagery, enabling future applications in:

* 🤖 Smart Farming
* 🚜 Autonomous Spraying Systems
* 🌿 Precision Agriculture
* 📷 Real-Time Field Monitoring

---

## 🎯 Objectives

* Build an automated weed detection model
* Train a YOLOv8 detector on annotated agricultural imagery
* Evaluate detection accuracy using standard object detection metrics
* Visualize model performance using training curves and confusion matrices

---

## 🛠️ Tech Stack

| Component                  | Technology   |
| -------------------------- | ------------ |
| Programming Language       | Python       |
| Object Detection Framework | YOLOv8       |
| Deep Learning Library      | PyTorch      |
| Dataset Management         | Roboflow     |
| Visualization              | Matplotlib   |
| Development Environment    | Google Colab |

---

## 📂 Dataset

The dataset was obtained from **Roboflow** and contains annotated agricultural images.

### Classes

* 🌱 Weeds
* 🌾 Other Vegetation (Undefined)

### Dataset Statistics

| Metric          | Value |
| --------------- | ----- |
| Training Images | 148   |
| Test Images     | 74    |
| Total Instances | 317   |
| Classes         | 2     |

---

# 📈 Model Performance

## Validation Results

| Metric    | Score     |
| --------- | --------- |
| Precision | **0.853** |
| Recall    | **0.817** |
| mAP@50    | **0.863** |
| mAP@50-95 | **0.612** |

## Test Results

| Metric    | Score     |
| --------- | --------- |
| Precision | **0.916** |
| Recall    | **0.890** |
| mAP@50    | **0.929** |
| mAP@50-95 | **0.699** |

---

## 🏆 Key Achievement

> The trained YOLOv8 model achieved **92.9% mAP@50** on the independent test dataset, demonstrating strong capability in detecting weeds under varying field conditions.

---

# 📊 Training Curves

<p align="center">
<img src="images/results.png" width="100%">
</p>

### Insights

✅ Training and validation losses consistently decreased throughout training.

✅ Precision improved from approximately 55% to 85%.

✅ Recall steadily increased across epochs.

✅ mAP@50 converged near 0.86 during validation.

These trends indicate successful model learning with minimal evidence of overfitting.

---

# 🔍 Confusion Matrix

<p align="center">
<img src="images/confusion_matrix.png" width="70%">
</p>

### Observations

* Most weed instances were correctly identified.
* Strong performance was achieved for the undefined vegetation class.
* Some confusion remains between weeds and surrounding vegetation due to visual similarity.

---

# 🚀 Training

```python
from ultralytics import YOLO

model = YOLO("yolov8s.pt")

model.train(
    data="data.yaml",
    epochs=50,
    imgsz=640,
    batch=16
)
```

---

# 📦 Installation

```bash
git clone https://github.com/yourusername/weed-detection-yolov8.git

cd weed-detection-yolov8

pip install -r requirements.txt
```

---

# 📁 Repository Structure

```text
weed-detection-yolov8/
│
├── README.md
├── requirements.txt
├── weed_detection_yoloV8.ipynb
│
├── images/
│   ├── results.png
│   ├── confusion_matrix.png
│   └── predictions.png
│
└── runs/
    └── detect/
```

---

# 🌍 Applications

* Precision Agriculture
* Smart Spraying Systems
* Weed Monitoring
* Crop Health Assessment
* Agricultural Robotics

---

# 🔮 Future Improvements

* Train on larger and more diverse agricultural datasets
* Experiment with YOLOv11 and RT-DETR architectures
* Deploy the model for real-time field detection
* Integrate drone and UAV imagery
* Develop precision spraying recommendations

---

# 👨‍💻 Author

### Stephen Adebisi

🎓 M.S. Geography (GIS)

🏫 South Dakota State University

### Research Interests

* Machine Learning
* Computer Vision
* Remote Sensing
* Precision Agriculture
* Spatial Data Science

---

## ⭐ Support

If you find this project useful, please consider giving the repository a **star ⭐**.

It helps increase visibility and supports future research and development.
