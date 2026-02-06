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

---

## 📑 Table of Contents
- Problem Statement  
- Solution Summary  
- Data Preprocessing Pipeline  
- Model Training Strategy  
- Inference Pipeline  
- System Architecture  
- Dataset  
- Technologies Used  
- Core Techniques  
- Evaluation Metrics  
- Business Value  
- Generative AI Module  
- Real-World Use Cases  
- Installation  
- Running the Notebook  
- Future Improvements  
- Author  

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

## 🔁 Data Preprocessing Pipeline

1. Resize images to 224×224  
2. Convert image to tensor  
3. Normalize using ImageNet mean & standard deviation  
4. Add batch dimension  

Normalization formula:

x_norm = (x - μ) / σ  

μ = (0.485, 0.456, 0.406)  
σ = (0.229, 0.224, 0.225)

---

## 🏋️ Model Training Strategy

- Backbone: ResNet-50 (ImageNet pretrained)  
- Final layer replaced with 2-class classifier  

### Transfer Learning Steps
1. Load pretrained ResNet-50  
2. Replace final fully connected layer  
3. Fine-tune on fruit dataset  

### Loss Function
Cross-Entropy Loss

### Optimizer
Adam

### Training Loop
Forward → Loss → Backpropagation → Weight Update  

Best model saved using validation performance.

---

## 🔮 Inference Pipeline

1. Load trained model  
2. Preprocess image  
3. Forward pass  
4. Softmax  
5. Select highest probability class  

---

## 🧠 System Architecture

```
Image → Preprocessing → ResNet-50 CNN → Prediction
                      ↘
          Feature Maps / Saliency / CAM
                      ↘
                Interpretation
```

---

## 📂 Dataset

- 234 images  
- Fruits: Apple, Mango, Tomato  
- Classes:
  - 0 = Fresh  
  - 1 = Rotten  

---

## ⚙️ Technologies Used

Python, PyTorch, Matplotlib, PIL, Diffusers, CUDA

---

## 🔍 Core Techniques

### Feature Hierarchy Visualization
Visualizes internal CNN representations.

### Feature Map Strip
Selects strongest channel per layer.

### Saliency Maps
Gradient-based pixel importance.

### Simplified CAM
Region-level class evidence.

---

## 📊 Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  

---

## 🏭 Business Value

- Automated quality inspection  
- Reduced labor cost  
- Reduced food waste  
- Consistent grading  
- Explainable decisions  

---

## 🧪 Generative AI Module (Stable Diffusion)

- Text-to-image synthesis  
- Dataset augmentation  
- Rare defect simulation  

Workflow:
Prompt → Diffusion Model → VAE Decoder → Image

---

## 🚀 Real-World Use Cases

- Packing plants  
- Supermarkets  
- Warehouses  
- Smart farms  

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
- Vision Transformers  
- Real-time camera deployment  
- Multi-class defects  

---

## 👨‍💻 Author

Fruit Guard Pro Team
