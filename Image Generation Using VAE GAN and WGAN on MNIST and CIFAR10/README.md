# Image Generation Using VAE, GAN, and WGAN on MNIST and CIFAR-10

## 📝 Overview

This project explores and compares three deep learning models for image generation:

- **Variational Autoencoders (VAE)**
- **Generative Adversarial Networks (GAN)**
- **Wasserstein GANs (WGAN)**

These models are implemented and evaluated on two benchmark datasets: **MNIST** and **CIFAR-10**. The focus is on understanding training behavior, image quality, and how model complexity and latent space size affect performance.

---

## 📦 Models Implemented

### 🔹 VAE (Variational Autoencoder)

- Encoder-decoder architecture
- Latent space regularized using KL-divergence
- Produces smooth reconstructions and allows interpolation

### 🔹 GAN (Generative Adversarial Network)

- Generator + Discriminator trained adversarially
- Binary cross-entropy loss
- Capable of generating realistic images, prone to mode collapse

### 🔹 WGAN (Wasserstein GAN)

- Uses a Critic instead of Discriminator
- Wasserstein loss (Earth Mover Distance)
- More stable training and improved diversity

---

## 📊 Datasets

### 🟢 MNIST
- 28x28 grayscale images of digits (0–9)
- 10 classes

### 🔵 CIFAR-10
- 32x32 color images
- 10 classes (airplane, car, cat, etc.)

---

## 🎯 Objective

- Compare the learning patterns and output quality of VAE, GAN, and WGAN
- Observe the impact of:
  - Latent space dimensions: `[5, 10, 50, 100]`
  - Model complexities: `[32, 64, 128, 256]`
- Use metrics like:
  - Reconstruction loss
  - Adversarial/Wasserstein loss
  - Image quality and diversity

---

## 🛠️ Implementation Details

### VAE

- Custom encoder and decoder using Conv layers
- Reconstruction loss + KL divergence
- Generates reconstructed images from latent vectors

### GAN

- Generator creates fake images from noise
- Discriminator classifies real vs fake
- Training uses binary cross-entropy
- Tracks Jensen-Shannon Divergence

### WGAN

- Critic estimates Wasserstein distance
- RMSprop optimizer and gradient clipping
- Earth Mover Distance (EMD) as metric

---

## 📈 Results Summary

### Latent Dimension Effects
- Smaller latent space → less expressive, smoother outputs
- Larger latent space → better details, risk of overfitting

### Model Complexity Effects
- Simple models → fast training, blurry images
- Complex models → sharp images, risk of instability (especially in GAN)

### Image Quality
- **VAE**: smooth but blurry
- **GAN**: sharp but unstable
- **WGAN**: stable with better visual diversity

---

## ✅ Conclusion

- **VAE** provides smooth and stable outputs but with slight blurriness.
- **GAN** achieves sharper images but suffers from training instability and mode collapse.
- **WGAN** delivers the most consistent and diverse results with stable convergence.
- **MNIST** is manageable with moderate model size; **CIFAR-10** requires deeper architectures and careful tuning.
- Latent dimension and model complexity critically impact output quality and training behavior.

---
