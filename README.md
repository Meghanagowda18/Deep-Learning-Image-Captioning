# 📸✨ Image Caption Generator

### *Deep Learning–Based System for Generating Descriptive Image Captions*

## 🚀 Overview

This project presents a complete deep-learning pipeline capable of converting images into meaningful, human-like captions. It combines **InceptionV3** (as a CNN-based encoder) with an **LSTM-based decoder**, enhanced using an **attention mechanism** that helps the model focus on important regions within an image.

The system is trained and fine-tuned on the **MS COCO dataset**, enabling it to generate coherent, context-aware descriptions for a wide range of real-world scenes.

---

## 🧠 Key Features

* Encoder–Decoder architecture using **InceptionV3 + LSTM**
* **Attention Mechanism** for improved focus on key image regions
* End-to-end training using paired images and captions
* Fine-tuning of CNN layers for enhanced visual understanding
* Evaluation using **BLEU Scores (quantitative)** and **manual inspection (qualitative)**
* Clean, modular code structure for easy experimentation and extensions

---

## 📂 Dataset — MS COCO

The MS COCO dataset is used for training and evaluation. It contains:

* **330,000+ images**
* **1.5M+ object instances**
* **80 object categories + 91 stuff categories**
* **5 human-written captions per image**

The dataset’s diversity and richness make it ideal for training models that need to understand real-world, multi-object scenes.

---

## 🛠️ Workflow Summary

### **1️⃣ Dataset Preparation**

* Images resized to **299×299** and normalized
* Captions tokenized, encoded, padded
* Vocabulary built using Keras **Tokenizer**

### **2️⃣ Feature Extraction (Encoder – CNN)**

A pre-trained **InceptionV3** model (without its classification head) extracts high-level visual features, producing compact image representations.

### **3️⃣ Caption Generation (Decoder – LSTM)**

An **LSTM-based decoder** takes the image features and generates captions sequentially, ensuring grammatical flow and context retention.

### **4️⃣ Attention Mechanism**

The attention layer allows the model to selectively focus on important areas of the image when predicting each word.

### **5️⃣ Training & Evaluation**

* **Optimizer:** Adam
* **Loss:** Categorical Cross-Entropy
* **Training/Validation split:** 80% / 20%
* **Evaluation:** BLEU Score + Human Review

### **6️⃣ Fine-Tuning**

* Unfreezing deeper CNN layers
* Data augmentation (rotation, zoom, flip)
* Leads to improved BLEU scores and more accurate captions

---

## 🔍 Results

### ⭐ Strengths

* Generates clear, context-aware, and grammatically correct captions
* Captures object relationships effectively
* Fine-tuned models show notably improved performance

### ⚠️ Challenges

* Difficulty with abstract or artistic images
* Struggles with subtle interactions (emotions, implied actions)
* Limited vocabulary for rare or unseen concepts

---

## 🧾 Project Structure

```
├── data/
│   ├── annotations.json
│   ├── images/
│   └── features/
├── src/
│   ├── extract_features.py
│   ├── preprocess_captions.py
│   ├── train_model.py
│   ├── evaluate.py
│   └── inference.py
├── tokenizer.json
├── captions_data.npz
└── README.md
```

---

## 📘 Technologies Used

* TensorFlow / Keras
* NumPy, Pandas
* **InceptionV3 (ImageNet)**
* LSTM & Attention Mechanism
* MS COCO Dataset

---

## 🌟 Conclusion

This project demonstrates how integrating CNNs and LSTMs—along with attention mechanisms—creates a powerful system for image captioning. The model performs well on common, natural scenes and establishes a strong foundation for future enhancements using modern multimodal architectures.

---

## 🔮 Future Work

* Integrate **Vision Transformers (ViT)**
* Explore transformer-based multimodal captioning models
* Expand dataset to include rare/abstract concepts
* Extend to **multilingual** caption generation

---

## 🙌 Team

**Team-D — EvoAstra Major Project**


