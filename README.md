# Child Abuse Meme Detection Using CLIP, ResNet50, and VGG16 in Zero-Shot, One-Shot, and Few-Shot Learning

## Introduction

The rapid growth of social media platforms has led to an increase in the circulation of harmful and abusive content in the form of memes. Memes combine visual and textual elements, making them an effective medium for spreading harmful messages. Among such content, child abuse-related memes are particularly concerning due to their potential psychological, social, and ethical impacts.

Traditional content moderation approaches often require large amounts of labeled data, which may not always be available for sensitive domains. Therefore, this project investigates the use of Zero-Shot, One-Shot, and Few-Shot learning techniques for detecting harmful child abuse memes using state-of-the-art computer vision and vision-language models.

---

## Motivation

Detecting harmful child abuse memes is challenging because:

- Limited labeled datasets are available.
- Harmful content can be expressed through subtle visual cues.
- Manual moderation is time-consuming and expensive.
- Early detection can help prevent the spread of harmful content.
- Modern platforms require scalable and automated moderation systems.

This project explores whether powerful pre-trained models can effectively detect harmful memes even when very little training data is available.

---

## Objectives

- Detect child abuse-related harmful memes.
- Compare traditional CNN models and vision-language models.
- Evaluate model performance under limited-data conditions.
- Analyze the effectiveness of Zero-Shot, One-Shot, and Few-Shot learning.
- Provide insights for future content moderation systems.

---

## Project Workflow

Dataset Collection
↓
Data Preprocessing
↓
Feature Extraction
↓
Model Implementation
(CLIP / ResNet50 / VGG16)
↓
Zero-Shot Learning
One-Shot Learning
Few-Shot Learning
↓
Model Evaluation
↓
Comparative Analysis

---

## Dataset

The dataset contains two classes:

### Harmful Memes
Memes containing content that promotes, glorifies, normalizes, or trivializes child abuse.

### Non-Harmful Memes
Memes that do not contain child abuse-related harmful content.

### Dataset Structure

```
dataset/
│
├── harmful/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── non_harmful/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

---

## Data Preprocessing

The following preprocessing steps were applied:

- Image resizing
- Pixel normalization
- Data cleaning
- Removal of corrupted images
- Train/Test split preparation
- Label encoding

### Image Transformations

- Resize to model input size
- Tensor conversion
- Mean-Std normalization

---

## Models Used

### 1. CLIP (Contrastive Language-Image Pretraining)

CLIP is a multimodal vision-language model developed by OpenAI.

#### Key Features

- Learns image-text relationships.
- Enables classification using text prompts.
- Performs well without task-specific training.
- Highly effective for Zero-Shot Learning.

#### Why CLIP?

Since harmful meme datasets are often limited, CLIP's pre-trained knowledge can help classify images without extensive training data.

---

### 2. ResNet50

ResNet50 is a deep Convolutional Neural Network containing 50 layers with residual connections.

#### Advantages

- Handles deep architectures effectively.
- Learns strong image representations.
- Widely used benchmark model.
- Suitable for transfer learning.

---

### 3. VGG16

VGG16 is a classical CNN architecture containing 16 learnable layers.

#### Advantages

- Simple architecture.
- Effective feature extraction.
- Strong baseline model.
- Easy to fine-tune.

---

## Learning Approaches

### Zero-Shot Learning

#### Definition

The model predicts classes without seeing any labeled examples during training.

#### Implementation

For CLIP:

- Generate text prompts such as:
  - "A harmful child abuse meme"
  - "A non-harmful meme"

- Compare image embeddings with text embeddings.

- Assign the class with highest similarity score.

#### Benefits

- No training required.
- Useful when labeled data is unavailable.

---

### One-Shot Learning

#### Definition

The model learns from only one example per class.

#### Implementation

- Select one labeled image from each class.
- Extract image embeddings.
- Compare test samples with support examples.
- Assign nearest class.

#### Benefits

- Requires minimal annotation effort.
- Suitable for rare classes.

---

### Few-Shot Learning

#### Definition

The model learns from a small number of labeled examples per class.

#### Implementation

- Use multiple support examples.
- Extract embeddings.
- Build class prototypes.
- Perform similarity-based classification.

#### Benefits

- Improved performance compared to One-Shot Learning.
- Effective in low-resource environments.

---

## Methodology

### Phase 1: Data Preparation

- Load dataset
- Organize class labels
- Apply image transformations

### Phase 2: Feature Extraction

#### CLIP

- Encode images
- Encode text prompts
- Generate image embeddings
- Generate text embeddings

#### ResNet50

- Remove classification head
- Extract feature vectors

#### VGG16

- Remove final classifier
- Extract deep image features

### Phase 3: Classification

#### Zero-Shot

Image → CLIP Embedding
↓
Compare with Text Embeddings
↓
Prediction

#### One-Shot

Support Image
↓
Feature Extraction
↓
Similarity Matching
↓
Prediction

#### Few-Shot

Support Set
↓
Feature Extraction
↓
Prototype Generation
↓
Similarity Matching
↓
Prediction

### Phase 4: Evaluation

Evaluate all models using:

- Accuracy
- Precision
- Recall
- F1-score

---

## Evaluation Metrics

### Accuracy

Measures overall correctness.

Accuracy = Correct Predictions / Total Predictions

### Precision

Measures prediction quality.

Precision = TP / (TP + FP)

### Recall

Measures detection capability.

Recall = TP / (TP + FN)

### F1 Score

Balances Precision and Recall.

F1 = 2 × (Precision × Recall) / (Precision + Recall)

---

## Experimental Setup

### Hardware

- CPU/GPU
- RAM
- Storage

### Software

- Python
- PyTorch
- Torchvision
- OpenCV
- NumPy
- Matplotlib
- CLIP

---

## Comparative Analysis

| Model | Zero-Shot | One-Shot | Few-Shot |
|---------|---------|---------|---------|
| CLIP | ✓ | ✓ | ✓ |
| ResNet50 | ✗ | ✓ | ✓ |
| VGG16 | ✗ | ✓ | ✓ |

CLIP naturally supports Zero-Shot classification through text-image alignment, whereas ResNet50 and VGG16 require support examples for One-Shot and Few-Shot learning.

---

## Applications

- Social media moderation
- Harmful content detection
- Online child safety
- AI-assisted moderation systems
- Digital platform governance

---

## Challenges

- Limited labeled data
- Sensitive content handling
- Dataset imbalance
- Visual ambiguity in memes
- Ethical concerns

---

## Ethical Considerations

This project is intended solely for research and content moderation purposes.

- Child abuse content can be disturbing.
- Predictions should not be used as the sole basis for moderation decisions.
- Human review remains essential.
- Data should be handled according to ethical and legal guidelines.

---

## Future Work

- Incorporate OCR for meme text extraction.
- Multimodal image-text fusion.
- Vision Transformers (ViT).
- Explainable AI methods.
- Larger benchmark datasets.
- Real-time moderation systems.

---

## Conclusion

This project investigates the effectiveness of CLIP, ResNet50, and VGG16 for detecting harmful child abuse memes under Zero-Shot, One-Shot, and Few-Shot learning settings. The study demonstrates how pre-trained vision-language and convolutional neural network models can assist content moderation systems when labeled data is scarce, contributing toward safer online environments and improved automated harmful content detection.
