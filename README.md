# 🛡️ Child Abuse Meme Detection using CLIP, ResNet50, and VGG16

<p align="center">

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red.svg)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow.svg)
![OpenCLIP](https://img.shields.io/badge/OpenCLIP-Vision--Language-green.svg)
![License](https://img.shields.io/badge/License-Research-lightgrey.svg)

</p>

---

## 📖 Overview

This repository presents a **multimodal deep learning framework** for detecting **child abuse-related harmful memes** using both convolutional neural networks and vision-language models.

Unlike traditional image classification tasks, harmful memes communicate abusive intent through the **interaction of images and embedded text**. Consequently, effective detection requires models capable of understanding both visual semantics and contextual relationships.

This project investigates the effectiveness of three state-of-the-art architectures:

- 🧠 CLIP (Contrastive Language–Image Pretraining)
- 🖼️ ResNet50
- 📷 VGG16

under low-resource learning settings including:

- Zero-Shot Learning
- One-Shot Learning
- Few-Shot Learning

The objective is to understand how these models perform when only limited labeled data is available, providing insights into practical multimodal content moderation systems.

---

# 📚 Table of Contents

- Overview
- Features
- Project Pipeline
- Models
- Learning Settings
- Repository Structure
- Pre-trained Models
- Installation
- Running Experiments
- Evaluation
- Results
- Research Motivation
- Contact
- Citation
- License

---

# ✨ Features

- 🔥 Multimodal harmful meme detection
- 🧠 Vision-language learning with CLIP
- 📷 CNN-based classification using ResNet50 and VGG16
- ⚡ Zero-Shot, One-Shot and Few-Shot experiments
- 📊 Comparative performance analysis
- 🔬 Reproducible research implementation
- 📒 Ready-to-run Jupyter notebooks
- 🚀 Pre-trained models available

---

# 🏗️ Project Pipeline

```
Input Meme
      │
      ▼
Image Preprocessing
      │
      ▼
Feature Extraction
      │
      ├───────────────┐
      │               │
      ▼               ▼
 CNN Models        CLIP Encoder
(ResNet/VGG)     (Vision-Language)
      │               │
      └───────────────┘
              │
              ▼
      Meme Classification
              │
              ▼
 Harmful / Non-Harmful
```

---

# 🧠 Models

| Model | Purpose |
|--------|---------|
| **CLIP** | Vision-language model capable of understanding both images and text using contrastive learning. Excellent for zero-shot classification. |
| **ResNet50** | Deep residual CNN for supervised image feature extraction and classification. |
| **VGG16** | Deep convolutional architecture with strong visual representation capabilities. |

---

# 🎯 Learning Settings

## Zero-Shot Learning

- No training on the target dataset
- Uses CLIP text prompts
- Direct image-text similarity prediction

---

## One-Shot Learning

- One labeled example per class
- Evaluates extreme low-resource learning

---

## Few-Shot Learning

- Small labeled training set
- Simulates practical real-world scenarios where annotation is expensive

---

# 📂 Repository Structure

```
Child-Abuse-Meme-Detection/
│
├── CLIP/
│   ├── Zero-Shot/
│   ├── One-Shot/
│   └── Few-Shot/
│
├── ResNet50/
│   ├── Zero-Shot/
│   ├── One-Shot/
│   └── Few-Shot/
│
├── VGG16/
│   ├── Zero-Shot/
│   ├── One-Shot/
│   └── Few-Shot/
│

---

# 📥 Pre-trained Models

GitHub restricts files larger than 100 MB. Therefore, all trained weights are hosted on Google Drive.

## Available Downloads

✔ CLIP

✔ ResNet50

✔ VGG16

✔ Training checkpoints

✔ Configuration files

**Google Drive**

https://drive.google.com/drive/folders/18FIXofA1L10hrVY9xccZy4CuDgqCPrh6

> Download the required model before running the notebooks.

---

# 🚀 Installation

```bash
git clone https://github.com/yourusername/Child-Abuse-Meme-Detection.git

cd Child-Abuse-Meme-Detection

pip install -r requirements.txt
```

---

# ▶ Running Experiments

Run the corresponding notebook depending on the experiment.

| Model | Zero-Shot | One-Shot | Few-Shot |
|--------|-----------|-----------|-----------|
| CLIP | ✅ | ✅ | ✅ |
| ResNet50 | ✅ | ✅ | ✅ |
| VGG16 | ✅ | ✅ | ✅ |

---

# 📈 Evaluation Metrics

Performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---



# 🔬 Research Motivation

Harmful memes remain challenging to detect because their meaning emerges from the interaction between textual and visual information.

CNNs excel at extracting visual features but cannot naturally understand embedded textual context. Vision-language models such as CLIP bridge this gap by jointly learning representations of images and language.

This project compares both paradigms under limited-data settings to understand their effectiveness for automated content moderation.

---

# 💻 Requirements

- Python 3.9+
- PyTorch
- Torchvision
- Transformers
- OpenCLIP
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

# 📬 Contact

**Palak Bhardwaj**

📧 bhardwajpalak777@gmail.com

Feel free to open an Issue or contact me regarding the project.

---

# 📖 Citation

If you use this repository in your research, please cite it appropriately.

```bibtex
@misc{childabusememe2026,
  author = {Palak Bhardwaj},
  title = {Child Abuse Meme Detection using CLIP, ResNet50 and VGG16},
  year = {2026},
  note = {GitHub Repository}
}
```

---


---

## ⭐ Support

If you found this repository helpful, please consider **starring ⭐ the repository**. It helps increase visibility and supports future research.
