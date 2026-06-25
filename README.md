# Child Abuse Meme Detection using CLIP, ResNet50, and VGG16

## Overview

This project presents a multimodal approach for detecting **child abuse-related harmful memes** using deep learning and vision-language models. Harmful memes often combine visual and textual content to convey abusive or inappropriate messages, making their automatic detection a challenging task. Accurate identification of such content is essential for improving online safety, supporting content moderation systems, and reducing the spread of harmful material across digital platforms.

The project evaluates the performance of three widely used models:

* **CLIP (Contrastive Language–Image Pretraining)**
* **ResNet50**
* **VGG16**

under different low-data learning scenarios, including:

* **Zero-Shot Learning**
* **One-Shot Learning**
* **Few-Shot Learning**

The objective is to analyze how effectively these models can identify harmful memes when only limited labeled training data is available.

---

## Pre-trained Model Downloads

Due to GitHub's file size limitations, the trained model weights and checkpoints are hosted on Google Drive.

### Google Drive

🔗 **Download Link:**
https://drive.google.com/drive/folders/18FIXofA1L10hrVY9xccZy4CuDgqCPrh6

The folder contains:

* CLIP model weights
* ResNet50 model weights
* VGG16 model weights
* Supporting checkpoints and configuration files

> **Note:** Please download the required model files before running the notebooks or evaluation scripts.

---

## Download Instructions

1. Open the Google Drive folder.
2. Download the required model archive:

   * CLIP
   * ResNet50
   * VGG16
3. Extract the downloaded archive.
4. Place the extracted model files in the appropriate project directories.
5. Run the corresponding notebooks or scripts for training or evaluation.

---

## Project Objectives

The primary objectives of this project are to:

* Detect child abuse-related harmful memes using deep learning models.
* Compare the performance of CNN-based and vision-language models.
* Evaluate model effectiveness under Zero-Shot, One-Shot, and Few-Shot learning settings.
* Analyze the impact of limited labeled data on harmful meme detection.
* Provide a benchmark for future research in multimodal harmful content detection.
