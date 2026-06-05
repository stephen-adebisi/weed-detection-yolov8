# Weed Detection in RGB Imagery Using YOLOv8

![Python](https://img.shields.io/badge/Python-3.12-blue)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-purple)
![mAP50](https://img.shields.io/badge/mAP%400.50-92.9%25-brightgreen)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)

An object detection pipeline using YOLOv8s to localize and classify weeds in RGB field imagery, trained on the [Krishibot Weed Detection Dataset](https://universe.roboflow.com/krishibot-mwqke/weed-detection-txujb) (741 images, 2 classes).

---

## Results

| Metric | Weeds | Undefined | Overall |
|--------|-------|-----------|---------|
| Precision | 0.875 | 0.958 | **0.916** |
| Recall | 0.946 | 0.835 | **0.890** |
| mAP@0.50 | 0.934 | 0.925 | **0.929** |
| mAP@0.50:0.95 | 0.679 | 0.719 | **0.699** |

Training converged in **50 epochs (~27 minutes)** on a Tesla T4 GPU.

---

## Sample Predictions

![Predictions](results/predictions.png)

---

## Training Curves

![Training Curves](results/results.png)

---

## Project Structure# weed-detection-yolov8
## Project Structure

| File | Description |
|------|-------------|
| `weed_detection.ipynb` | Full pipeline notebook |
| `weights/best.pt` | Trained model weights |
| `results/results.png` | Training curves |
| `results/confusion_matrix.png` | Confusion matrix |
| `results/PR_curve.png` | Precision-Recall curve |
| `results/predictions.png` | Sample predictions on test images |
