# image-super-resolution

# 4x Image Super-Resolution with SwinIR

This project implements a **deep learning pipeline** for 4× image super-resolution using the **SwinIR** (Swin Transformer for Image Restoration) model. It includes custom dataset handling, data augmentation, a multi-component loss function, and evaluation using PSNR and SSIM metrics.

---

# About the Model – SwinIR

**SwinIR** (Swin Transformer for Image Restoration) is a vision transformer-based model that introduces:

- **Shifted window attention**: Local self-attention with cross-window context
- **Hierarchical structure**: Efficient scaling across different resolution levels
- **PixelShuffle Upsampling**: Lightweight and fast image reconstruction

The architecture adapts transformer blocks for image-to-image tasks and is state-of-the-art on datasets like Set5, Set14, and Urban100.

> More details: [SwinIR Paper](https://arxiv.org/abs/2108.10257)

---
Training Visualisation of Loss

<img width="822" alt="image" src="https://github.com/user-attachments/assets/37ab57c2-8086-4fe8-8fc0-56d21c9f054d" />

---

## Project Overview

- **Model**: SwinIR (pre-trained weights finetuned)
- **Upscaling Factor**: ×4
- **Framework**: PyTorch
- **Loss Function**: L1 + SSIM + VGG perceptual loss
- **Evaluation Metrics**: PSNR, SSIM

---


## Features

-  Custom `Dataset` class with random cropping and strong data augmentation
-  Fine-tuning of a pre-trained SwinIR model
-  Combined loss: L1 + SSIM + VGG Perceptual Loss
-  Evaluation using PSNR and SSIM
-  Best model checkpoint saving

---

## Results 

The SwinIR output was compared to Bicubic 4x image resolution. 

![image](https://github.com/user-attachments/assets/bc2f0397-b042-4fc5-8971-d08d134f31dd)

![image](https://github.com/user-attachments/assets/be489c66-5079-454e-a79e-2d0c105da623)

![image](https://github.com/user-attachments/assets/28ad49e8-b5a0-4e70-a910-7b2e7c643912)



