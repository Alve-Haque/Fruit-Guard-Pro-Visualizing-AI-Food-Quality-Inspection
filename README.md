# 🍎🥭🍅 Fruit Guard Pro  
### Visualizing AI-Powered Food Quality Inspection  
**Interpretable Deep Learning for Fresh vs. Rotten Fruit Classification**

---

## 📑 Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [System Architecture](#system-architecture)
- [Dataset](#dataset)
- [Data Preprocessing Pipeline](#data-preprocessing-pipeline)
- [Model Architecture](#model-architecture)
- [Model Training Strategy](#model-training-strategy)
- [Inference Pipeline](#inference-pipeline)
- [Interpretability & Visualization](#interpretability--visualization)
- [Generative AI Module](#generative-ai-module)
- [Evaluation Metrics](#evaluation-metrics)
- [Business Value](#business-value)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## Overview

Fruit Guard Pro is an end-to-end deep learning system for automated fruit quality inspection.  
The system classifies fruit images as **Fresh** or **Rotten** and explains its decisions using modern interpretability techniques.

Unlike traditional black-box models, Fruit Guard Pro provides visual insight into:

- What features the CNN learns  
- Which pixels influence predictions  
- Which regions drive classification  
- How synthetic images can be generated using Generative AI  

This makes the system reliable, transparent, and suitable for real-world deployment.

---

## Problem Statement

Manual fruit inspection is:

- Slow  
- Subjective  
- Expensive  

There is a need for an automated system that can inspect fruit quickly, consistently, and accurately while also providing explanations.

---

## Project Objectives

- Build a CNN-based fruit classifier  
- Visualize internal feature representations  
- Generate saliency and CAM heatmaps  
- Enable synthetic image generation  
- Demonstrate explainable AI in agriculture  

---

## System Architecture

```
Input Image
   |
Preprocessing
   |
ResNet-50 CNN
   |
Prediction (Fresh / Rotten)
   |
----------------------------
| Feature Maps            |
| Saliency Maps           |
| Class Activation Maps   |
----------------------------
   |
Interpretation
```

---

## Dataset

- 234 fruit images  
- Fruits: Apple, Mango, Tomato  
- Classes:
  - 0 → Fresh  
  - 1 → Rotten  

---

## Data Preprocessing Pipeline

1. Resize images to 224 × 224  
2. Convert to PyTorch tensors  
3. Normalize using ImageNet statistics  
4. Add batch dimension  

---

## Model Architecture

- Backbone: ResNet-50  
- Pretrained on ImageNet  
- Final fully connected layer replaced with 2-class output  

---

## Model Training Strategy

- Transfer Learning  
- Cross-Entropy Loss  
- Adam Optimizer  

---

## Inference Pipeline

1. Load trained model  
2. Preprocess input image  
3. Forward pass  
4. Apply Softmax  
5. Choose highest probability class  

---

## Interpretability & Visualization

### Feature Hierarchy Visualization
Shows how representations evolve through CNN layers.

### Feature Map Strip
Selects strongest activation channel per layer.

### Saliency Maps
Gradient-based pixel importance.

### Class Activation Maps (CAM)
Highlights regions responsible for classification.

---

## Generative AI Module

Uses Stable Diffusion for text-to-image generation.

---

## Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  

---

## Business Value

- Reduces labor cost  
- Improves quality consistency  
- Reduces food waste  
- Builds trust through explainability  
- Scalable deployment  

---

## Technologies Used

- Python  
- PyTorch  
- Matplotlib  
- PIL  
- Diffusers  
- CUDA  

---

## Installation

```bash
git clone https://github.com/yourusername/fruit-guard-pro.git
cd fruit-guard-pro
pip install -r requirements.txt
```

---

## Running the Project

```bash
jupyter notebook C3M2_Assignment.ipynb
```

---

## Future Improvements

- Grad-CAM++  
- Vision Transformers  
- Real-time camera integration  
- Multiclass defect detection  

---

## Author

Fruit Guard Pro Team


---

## 🤖 Generative AI Module (Stable Diffusion)

Fruit Guard Pro also includes an optional **Generative AI component** based on **Stable Diffusion** for text-to-image synthesis.

### Purpose

- Generate synthetic fruit images  
- Augment small datasets  
- Simulate rare or hard-to-capture defects  
- Improve model robustness  

### Workflow

```
Text Prompt
     ↓
Latent Noise Initialization
     ↓
Iterative Denoising (Diffusion Model)
     ↓
VAE Decoder
     ↓
Synthetic Fruit Image
```

### Example Prompt

```
A mango with a small hole made by a worm in the middle
```

### How Generative AI Connects to Classification

- Generated images can be added to the training dataset  
- Used to test model behavior on rare defects  
- Helps analyze failure cases  

This creates a continuous improvement loop:

```
Generation → Training → Interpretation → Model Improvement
```

