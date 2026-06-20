# Child Abuse Meme Detection using CLIP, ResNet50, and VGG16

## Overview

This project focuses on the detection of **child abuse-related harmful memes** using deep learning and vision-language models. Child abuse content can be harmful, distressing, and potentially dangerous, making its identification important for content moderation and online safety.

The project investigates the effectiveness of:

- CLIP (Contrastive Language–Image Pretraining)
- ResNet50
- VGG16

under:

- Zero-Shot Learning
- One-Shot Learning
- Few-Shot Learning

to determine how well these models can classify harmful content when limited labeled data is available.

---

## Motivation

The increasing use of memes on social media platforms has made harmful content more difficult to identify using traditional moderation techniques. Child abuse-related memes may normalize, glorify, or trivialize abusive behavior and can have serious social consequences.

Challenges include:

- Limited availability of labeled datasets
- High annotation cost
- Sensitive nature of the content
- Need for scalable moderation systems
- Difficulty in detecting subtle visual cues

This project explores whether powerful pre-trained models can effectively detect harmful memes in low-data scenarios.

---

## Objectives

- Detect child abuse-related harmful memes.
- Evaluate the effectiveness of CLIP, ResNet50, and VGG16.
- Explore Zero-Shot, One-Shot, and Few-Shot learning approaches.
- Analyze model performance under limited-data conditions.
- Support research in automated harmful content moderation.

---

## Self-Curated Dataset

A self-curated dataset was developed specifically for this project.

### Dataset Collection

- Memes were collected from publicly available online sources.
- Images were manually reviewed and filtered.
- Samples were categorized according to their content.
- Dataset quality was maintained through manual verification.

### Classes

#### Harmful Child Abuse Memes

Memes containing content that promotes, glorifies, normalizes, trivializes, or encourages child abuse-related behavior.

#### Non-Harmful Memes

Memes that do not contain child abuse-related harmful content and serve as negative examples.

### Annotation Process

- Images were manually labeled.
- Labels were reviewed for consistency.
- Ambiguous samples were re-evaluated before inclusion.

### Dataset Characteristics

- Binary classification dataset
- Image-based meme collection
- Designed for low-data learning experiments
- Suitable for Zero-Shot, One-Shot, and Few-Shot evaluation

### Importance of the Dataset

Publicly available datasets for child abuse meme detection are extremely limited. Therefore, a self-curated dataset was developed to facilitate research in harmful content detection and online safety.

---

## Project Workflow

```text
Dataset Collection
        ↓
Data Annotation
        ↓
Data Preprocessing
        ↓
Feature Extraction
        ↓
Model Implementation
(CLIP, ResNet50, VGG16)
        ↓
Zero-Shot Learning
One-Shot Learning
Few-Shot Learning
        ↓
Model Evaluation
        ↓
Performance Analysis
```

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Image resizing
- Image normalization
- Data cleaning
- Removal of corrupted samples
- Label encoding
- Dataset organization

### Transformations

- Resize images to model input dimensions
- Convert images to tensors
- Normalize pixel values

---

## Models Used

### CLIP

CLIP (Contrastive Language–Image Pretraining) is a vision-language model that learns relationships between images and text.

#### Features

- Uses image-text alignment
- Supports Zero-Shot classification
- Requires minimal task-specific training
- Learns generalized visual representations

#### Why CLIP?

CLIP can classify images using natural language prompts, making it highly suitable for scenarios with little or no labeled data.

---

### ResNet50

ResNet50 is a deep convolutional neural network containing residual connections that allow effective training of deep architectures.

#### Features

- Deep feature extraction
- Strong transfer learning performance
- Robust image representation learning

---

### VGG16

VGG16 is a classical convolutional neural network architecture widely used for image classification tasks.

#### Features

- Simple architecture
- Effective feature extraction
- Strong baseline performance

---

## Learning Approaches

### Zero-Shot Learning

Zero-Shot Learning allows a model to classify data without seeing any task-specific training examples.

#### CLIP Implementation

Example prompts:

- "A harmful child abuse meme"
- "A non-harmful meme"

The image embedding is compared against text embeddings, and the class with the highest similarity score is selected.

#### Benefits

- No training required
- Useful when labeled data is unavailable

---

### One-Shot Learning

One-Shot Learning uses a single labeled example per class.

#### Method

- Select one support image per class.
- Extract feature embeddings.
- Compare test samples with support samples.
- Assign the nearest class.

#### Benefits

- Minimal annotation effort
- Suitable for rare classes

---

### Few-Shot Learning

Few-Shot Learning uses a small number of labeled examples per class.

#### Method

- Use multiple support examples.
- Extract embeddings.
- Create class prototypes.
- Classify based on similarity.

#### Benefits

- Better performance than One-Shot Learning
- Effective in low-resource environments

---

## Methodology

### Phase 1: Data Preparation

- Load dataset
- Organize classes
- Apply preprocessing transformations

### Phase 2: Feature Extraction

#### CLIP

- Encode images
- Encode text prompts
- Generate image embeddings
- Generate text embeddings

#### ResNet50

- Remove classification layer
- Extract visual feature vectors

#### VGG16

- Remove final classifier
- Extract deep image features

### Phase 3: Classification

#### Zero-Shot Pipeline

```text
Image
  ↓
CLIP Encoder
  ↓
Text Prompt Matching
  ↓
Prediction
```

#### One-Shot Pipeline

```text
Support Image
     ↓
Feature Extraction
     ↓
Similarity Matching
     ↓
Prediction
```

#### Few-Shot Pipeline

```text
Support Set
     ↓
Feature Extraction
     ↓
Prototype Creation
     ↓
Similarity Matching
     ↓
Prediction
```

### Phase 4: Evaluation

Model performance is evaluated using standard classification metrics.

---

## Evaluation Metrics

### Accuracy

Measures overall prediction correctness.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Measures prediction quality.

```text
Precision = TP / (TP + FP)
```

### Recall

Measures the ability to identify harmful memes.

```text
Recall = TP / (TP + FN)
```

### F1-Score

Balances Precision and Recall.

```text
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

---

## Technologies Used

- Python
- PyTorch
- Torchvision
- OpenCV
- NumPy
- Matplotlib
- CLIP

---

## Applications

- Social media moderation
- Harmful content detection
- Online child safety systems
- AI-assisted moderation
- Content filtering platforms

---

## Challenges

- Limited labeled data
- Sensitive content handling
- Class imbalance
- Visual ambiguity in memes
- Ethical and legal concerns

---

## Ethical Considerations

This project is intended exclusively for research and educational purposes related to content moderation and online safety.

- Child abuse content can be emotionally distressing.
- The system is designed to assist moderation efforts.
- Human oversight remains necessary for sensitive decisions.
- Data should be handled responsibly and ethically.

---

## Future Work

- OCR-based text extraction from memes
- Multimodal image-text fusion
- Vision Transformer (ViT) architectures
- Explainable AI techniques
- Larger benchmark datasets
- Real-time moderation systems

---

## Disclaimer

This project focuses on the detection of child abuse-related harmful memes for research, safety, and moderation purposes. The inclusion of such content does not imply endorsement, promotion, or support of abusive behavior. The objective is to develop automated systems that assist in identifying and reducing the spread of harmful online content.

---

## Conclusion

This project investigates the effectiveness of CLIP, ResNet50, and VGG16 for detecting child abuse-related harmful memes under Zero-Shot, One-Shot, and Few-Shot learning settings. By leveraging pre-trained vision-language and convolutional neural network models, the study demonstrates approaches for harmful content detection in scenarios where labeled data is limited, contributing to safer online environments and more effective content moderation systems.
