# 🧠 Generative Adversarial Network (GAN) on MNIST

## 📌 Project Overview

This project implements a **Generative Adversarial Network (GAN)** using **TensorFlow (Keras API)** to generate handwritten digit images similar to the MNIST dataset.

A GAN consists of two neural networks trained adversarially:

- **Generator** – Generates synthetic digit images from random noise.
- **Discriminator** – Classifies images as real (from dataset) or fake (generated).

The generator learns to fool the discriminator, while the discriminator learns to detect fake images.

---

## 📂 Dataset

The model is trained on the **MNIST dataset**, which contains:

- 60,000 training images  
- 28 × 28 grayscale handwritten digit images (0–9)

### 🔹 Preprocessing Steps

- Normalized pixel values to the range **[-1, 1]**
- Reshaped images to **(28, 28, 1)**
- Created shuffled batches using TensorFlow Dataset API

---

## 🏗️ Model Architecture

### 🔹 Generator Network

- Dense Layer (7×7×256)
- Batch Normalization
- LeakyReLU
- Reshape Layer
- Conv2DTranspose
- Batch Normalization
- LeakyReLU
- Conv2DTranspose
- Output Layer (Tanh activation)

**Input:** 100-dimensional random noise vector  
**Output:** 28×28 grayscale image  

---

### 🔹 Discriminator Network

- Conv2D
- LeakyReLU
- Dropout
- Conv2D
- LeakyReLU
- Dropout
- Flatten
- Dense (Sigmoid activation)

**Output:** Probability of image being real or fake  

---

## ⚙️ Training Configuration

- **Epochs:** 20  
- **Batch Size:** 128  
- **Noise Dimension:** 100  
- **Loss Function:** Binary Cross-Entropy (BCE)  
- **Optimizer:** Adam (learning rate = 0.0002, β₁ = 0.5)  

---

## 📊 Results

Images of generated Digit Samples and Loss curve are attached here

---

## 🎯 Key Learning Outcomes
- Understanding adversarial learning
- Implementing GAN architecture in TensorFlow
- Handling GAN training instability
- Generator vs Discriminator dynamics
- Visual evaluation of generative models

---

##🔮 Future Improvements

- Conditional GAN (digit-specific generation)
- Wasserstein GAN for improved stability
- FID score evaluation for quantitative analysis

---
## 👩‍💻 Author

Fathima Salga
AI & GenAI Assignment
Year: 2026



