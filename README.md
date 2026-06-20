# 🖼️ Image Classification with Lobe.ai + TensorFlow

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-SavedModel-FF6F00?logo=tensorflow&logoColor=white)
![Lobe.ai](https://img.shields.io/badge/Lobe.ai-No--Code%20ML-6C2BD9)
![License](https://img.shields.io/badge/license-MIT-green)

> A no-code image classification project built using Microsoft's Lobe.ai — images collected, labelled, and trained visually in Lobe, then exported as a TensorFlow SavedModel and run via Python inference script.

---

## 📌 Table of Contents

- [About](#about)
- [How It Works](#how-it-works)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Getting Started](#getting-started)
- [Running Inference](#running-inference)
- [Lab Report](#lab-report)
- [About the Author](#about-the-author)

---

## About

This project demonstrates end-to-end image classification using **Lobe.ai** — Microsoft's drag-and-drop ML training tool. Images are collected and labelled by class inside the Lobe desktop app, which trains a custom TensorFlow model automatically. The trained model is exported and run locally using the `lobe-python` inference library.

Built as **Lab 5** for GITAM University's AI/ML coursework.

> Update this section with your specific classification classes (e.g. "classifies hand gestures into Rock / Paper / Scissors").

---

## How It Works

```
1. Collect images  →  2. Label by class in Lobe.ai  →  3. Auto-train TF model
       ↓
4. Export as TensorFlow SavedModel
       ↓
5. Run predict.py to classify new images
```

Lobe.ai handles the full training pipeline — no manual model architecture or hyperparameter tuning required.

---

## Tech Stack

| Component     | Technology                    |
|---------------|-------------------------------|
| ML Tool       | Microsoft Lobe.ai             |
| Model Format  | TensorFlow 2.x (SavedModel)   |
| Inference     | `lobe-python` library         |
| Language      | Python 3.7+                   |
| Lab Docs      | DOCX / PDF                    |

## Getting Started

### Prerequisites

- Python 3.7–3.10
- [Lobe desktop app](https://www.lobe.ai/) (for retraining only)

### Installation

```bash
# Clone
git clone https://github.com/ShivaGunuru/Lobe.ai-Image-classification-.git
cd Lobe.ai-Image-classification-

# Create virtual environment
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate

# Install dependencies
pip install lobe
```

Or via `requirements.txt`:

```bash
pip install -r requirements.txt
```

**`requirements.txt`:**

```
lobe>=0.5.0
Pillow
```

---

## Running Inference

```bash
cd "trained model(tensor flow)"
python predict.py
```

Or call from Python directly:

```python
from lobe import ImageModel

# Load the exported model
model = ImageModel.load('../trained model(tensor flow)')

# Predict on an image
result = model.predict_from_file('path/to/image.jpg')

print(result.prediction)       # predicted class label
print(result.labels)           # all labels with confidence scores
```

---

## Lab Report

Full lab documentation (methodology, screenshots, results) is available:

- [`Labs_5.pdf`](./Labs_5.pdf)
- [`Labs_5.docx`](./Labs_5.docx)

---

## About the Author

**Gunuru Venkata Shiva Kumar**
B.Tech CSE | GITAM University, Visakhapatnam (CGPA: 8.99)

- 📧 shiva.gunuru@gmail.com
- 🔗 [GitHub](https://github.com/ShivaGunuru)
- 🔗 [LinkedIn](https://linkedin.com/in/shiva-gunuru)
