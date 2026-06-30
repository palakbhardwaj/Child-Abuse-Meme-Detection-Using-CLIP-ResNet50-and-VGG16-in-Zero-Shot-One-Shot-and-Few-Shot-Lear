# Child Abuse Meme Detection using CLIP, ResNet50, and VGG16

## 🛡️ Overview

This project presents a **multimodal framework for detecting child abuse-related harmful memes** using state-of-the-art deep learning and vision-language models. Harmful memes often communicate abusive or inappropriate content by combining **images and text**, making them significantly more challenging to detect than traditional text-only or image-only content.

Automatic identification of such content is crucial for enhancing **online safety**, supporting **content moderation**, protecting vulnerable users, and reducing the spread of harmful material across social media platforms.

This repository investigates and compares the effectiveness of three powerful models:

* **CLIP (Contrastive Language–Image Pretraining)**
* **ResNet50**
* **VGG16**

under various **low-data learning scenarios**, where only a limited number of labeled examples are available.

The experiments are conducted using:

* **Zero-Shot Learning**
* **One-Shot Learning**
* **Few-Shot Learning**

The goal is to evaluate how well these models can recognize harmful memes with minimal supervision and analyze their suitability for real-world moderation systems.

---

# ✨ Features

* 🖼️ Multimodal harmful meme detection
* 🤖 Comparison of CNN and Vision-Language models
* ⚡ Zero-Shot inference using CLIP
* 📚 One-Shot and Few-Shot learning experiments
* 📊 Performance comparison across multiple settings
* 🔬 Benchmark for child abuse meme detection research
* 🚀 Easy-to-run Jupyter notebooks

---

# 🧠 Models Used

| Model        | Description                                                                                                                                     |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **CLIP**     | Vision-language model capable of learning semantic relationships between images and text, enabling strong zero-shot classification performance. |
| **ResNet50** | Deep residual convolutional neural network used as a powerful image feature extractor for supervised classification.                            |
| **VGG16**    | Classic convolutional neural network architecture known for its simplicity and strong feature representation capabilities.                      |

---

# 🎯 Learning Settings

The project evaluates model performance under different data availability scenarios:

### Zero-Shot Learning

* No task-specific training data is used.
* CLIP predicts classes directly using image-text similarity.

### One-Shot Learning

* Models are trained using only **one labeled example per class**.

### Few-Shot Learning

* Models learn from a small number of labeled examples, simulating realistic low-resource environments.

---

# 📂 Repository Structure

```text
Child-Abuse-Meme-Detection/
│
├── CLIP/
│   ├── Zero-Shot/
│   ├── One-Shot/
│   └── Few-Shot/
│
├── ResNet50/
│   ├── One-Shot/
│   └── Few-Shot/
     ── Zero-Shot/
│
├── VGG16/
│   ├── One-Shot/
│   └── Few-Shot/
│    ── Zero-Shot/

```

---

# 📥 Pre-trained Model Downloads

Due to GitHub's file size limitations, the trained model weights and checkpoints are hosted on **Google Drive**.

### 📁 Google Drive

🔗 **Model Download Link**

[https://drive.google.com/drive/folders/18FIXofA1L10hrVY9xccZy4CuDgqCPrh6](https://drive.google.com/drive/folders/18FIXofA1L10hrVY9xccZy4CuDgqCPrh6)

The folder contains:

* ✅ CLIP model weights
* ✅ ResNet50 model weights
* ✅ VGG16 model weights
* ✅ Training checkpoints
* ✅ Configuration files

> **Note:** Please download the required model files before running the notebooks or evaluation scripts.

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/Child-Abuse-Meme-Detection.git

cd Child-Abuse-Meme-Detection
```

---

## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3. Download Pre-trained Models

Download the required model weights from the Google Drive folder and place them inside the appropriate model directories.

Example:

```text
models/
├── CLIP/
├── ResNet50/
└── VGG16/
```

---

## 4. Run Experiments

Open the corresponding notebook for the desired model and learning setting.

Examples:

* CLIP Zero-Shot
* CLIP One-Shot
* CLIP Few-Shot
* ResNet50 One-Shot
* ResNet50 Few-Shot
* VGG16 One-Shot
* VGG16 Few-Shot

---

# 📊 Project Objectives

This project aims to:

* Detect child abuse-related harmful memes using deep learning techniques.
* Compare CNN-based and vision-language models for multimodal content understanding.
* Evaluate model performance under Zero-Shot, One-Shot, and Few-Shot learning scenarios.
* Analyze the impact of limited labeled data on harmful meme detection.
* Explore the effectiveness of multimodal representations for online content moderation.
* Provide a reproducible benchmark for future research on harmful meme detection.

---

# 📈 Evaluation

Model performance can be evaluated using common classification metrics such as:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

The repository includes notebooks for training, testing, and performance analysis.

---

# 💻 Requirements

Typical dependencies include:

```text
Python 3.9+
PyTorch
Torchvision
Transformers
OpenCLIP
NumPy
Pandas
Matplotlib
Scikit-learn
Jupyter Notebook
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

# 🔬 Research Motivation

Detecting child abuse-related memes remains a challenging task because harmful intent often emerges from the interaction between visual content and embedded text. Traditional image classification models may fail to capture this multimodal context, while vision-language models such as CLIP can better understand semantic relationships across modalities. This project investigates the strengths and limitations of both approaches under low-resource learning conditions.

---

# 📬 Contact

If you need access to additional resources or have any questions regarding the project, feel free to contact:

**Palak Bhardwaj**

📧 **[bhardwahpalak777@gmail.com](mailto:bhardwahpalak777@gmail.com)**

---

# 📄 License

This project is intended for **research and educational purposes only**. The dataset and trained models should be used responsibly and in accordance with applicable ethical guidelines and data usage policies.

---

⭐ **If you find this project useful, consider giving the repository a star to support future research and development.**
