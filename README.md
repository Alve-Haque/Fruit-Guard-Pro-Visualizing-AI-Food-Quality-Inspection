# 🍎🥭🍅 Fruit Guard Pro  
### Visualizing AI-Powered Food Quality Inspection  
**Interpretable Deep Learning for Fresh vs. Rotten Fruit Classification**

---

## 🌟 Overview

**Fruit Guard Pro** is an end-to-end deep learning project that demonstrates how **Convolutional Neural Networks (CNNs)** can be used not only to classify fruit quality (fresh vs. rotten), but also to **explain their own decisions** through powerful visualization and interpretability techniques.

Instead of treating the model as a black box, this project opens it up—showing:

- How features evolve inside the network  
- Which pixels influence predictions  
- Which regions drive final decisions  
- How generative AI can synthesize realistic fruit images  

This makes the system suitable for **real-world deployment**, where trust, transparency, and explainability are essential.


## 📑 Table of Contents
- [Problem Statement](#-problem-statement)
- [Solution Summary](#-solution-summary)
- [System Architecture](#-system-architecture)
- [Dataset](#-dataset)
- [Technologies Used](#-technologies-used)
- [Core Techniques](#-core-techniques)
- [Evaluation Metrics](#-evaluation-metrics)
- [Business Value](#-business-value)
- [Real-World Use Cases](#-real-world-use-cases)
- [Installation](#-installation)
- [Running the Notebook](#-running-the-notebook)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 🎯 Problem Statement

Manual inspection of fruit quality is:

- Time-consuming  
- Subjective  
- Expensive at scale  

The goal is to build an **automated vision-based inspection system** that:

1. Classifies fruit as **Fresh** or **Rotten**
2. Explains *why* the model made each decision
3. Provides visual tools for debugging and improvement

---

## 💡 Solution Summary

Fruit Guard Pro combines:

- A **pretrained ResNet-50 CNN**
- Gradient-based interpretability methods
- Activation-based visualization techniques
- Optional **Stable Diffusion** image generation

Together, these create a transparent and auditable AI pipeline.

---

## 🧠 System Architecture

```
Input Image (224×224 RGB)
        |
   Preprocessing
        |
   ResNet-50 CNN
        |
+-----------------------------+
| Feature Maps               |
| Saliency Maps              |
| Class Activation Maps      |
+-----------------------------+
        |
 Fresh / Rotten Prediction
```

---

## 📂 Dataset

- 234 images (subset)
- Fruits: Apples, Mangoes, Tomatoes  
- Classes:
  - `0` → Fresh  
  - `1` → Rotten  

---

## ⚙️ Technologies Used

| Category | Tools |
|--------|------|
| Language | Python |
| Deep Learning | PyTorch |
| Vision Models | ResNet-50 |
| Visualization | Matplotlib |
| Image Processing | PIL |
| Generative AI (Optional) | Stable Diffusion (diffusers) |
| Hardware Acceleration | CUDA / GPU |

---

## 🔍 Core Techniques

### 1️⃣ Feature Hierarchy Visualization
### 2️⃣ Feature Map Strip
### 3️⃣ Saliency Maps (Gradient-Based)
### 4️⃣ Simplified Class Activation Maps (CAM)
### 5️⃣ Stable Diffusion Image Generation (Optional)

---

## 📊 Evaluation Metrics

Accuracy, Precision, Recall, F1-score, Confusion Matrix

---

## 🏭 Business Value

- Cost Reduction  
- Quality Assurance  
- Trust & Compliance  
- Scalability  
- Data Augmentation  

---

## 🚀 Real-World Use Cases

- Fruit packaging plants  
- Supermarket sorting lines  
- Cold storage warehouses  
- Agricultural research  
- Smart farming systems  

---

## 🛠️ Installation

```bash
git clone https://github.com/yourusername/fruit-guard-pro.git
cd fruit-guard-pro
pip install -r requirements.txt
```

---

## ▶️ Running the Notebook

```bash
jupyter notebook C3M2_Assignment.ipynb
```

---

## 🔮 Future Improvements

- Grad-CAM++  
- Vision Transformers (ViT)  
- Multiclass defect detection  
- Real-time camera integration  

---

## 👨‍💻 Author

Fruit Guard Pro Team
