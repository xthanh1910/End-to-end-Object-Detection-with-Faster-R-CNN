# PASCAL VOC Object Detection with Faster R-CNN

This repository implements an efficient object detection pipeline using the **Faster R-CNN** architecture with a **MobileNetV3-Large** backbone. The model is trained and evaluated on the **PASCAL VOC 2012** dataset, balancing detection accuracy with inference speed.

---

## Video Demo

Click the images below to watch the model in action on various video samples:

<div align="center">
  <a href="https://www.youtube.com/watch?v=hdipd4-nzAM">
    <img src="https://img.youtube.com/vi/hdipd4-nzAM/0.jpg" alt="Video Demo 1" style="width:45%;">
  </a>
  <a href="https://www.youtube.com/watch?v=KT_-X-a4BnE">
    <img src="https://img.youtube.com/vi/KT_-X-a4BnE/0.jpg" alt="Video Demo 2" style="width:45%;">
  </a>
</div>

---

## Detection Samples

Below are some example predictions on the PASCAL VOC test set:

<div align="center">
  <img src="demo/1.png" width="45%"> <img src="demo/2.png" width="45%">
  <br>
  <img src="demo/3.png" width="45%"> <img src="demo/4.png" width="45%">
</div>

---

## Features

* **Architecture**: Faster R-CNN with a MobileNetV3-Large-320 FPN backbone for lightweight yet powerful feature extraction.
* **Data Augmentation**: Robust training pipeline including `RandomAffine` (rotation, translation, scale, shear) and `ColorJitter` (brightness, contrast, saturation) to improve generalization.
* **Comprehensive Evaluation**: Built-in support for **Mean Average Precision (mAP)** calculation using `torchmetrics`.
* **Flexible Inference**: Dedicated scripts for both static image detection and real-time video processing.
* **Experiment Tracking**: Integrated with **TensorBoard** for monitoring loss curves and mAP metrics during training.

---

## Project Structure

* `voc_dataset.py`: Custom dataset class to handle PASCAL VOC XML annotations and category mapping.
* `train_fasterrcnn.py`: The main training engine including the loop, validation, and checkpoint saving.
* `test_image_fasterrcnn.py`: Inference script for single image detection.
* `test_video_fasterrcnn.py`: Inference script for processing video files and saving results.

---
