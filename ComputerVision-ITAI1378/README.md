# Computer Vision — ITAI 1378

**Houston Community College | Spring 2026**  
**Instructor Course:** ITAI 1378 — Introduction to Computer Vision

---

## Overview

This section of my AI portfolio covers projects completed in ITAI 1378. The course focuses on applying computer vision techniques using PyTorch and torchvision, including image classification, transfer learning, and model evaluation.

---

## Projects

### 🍽️ [Food Classification — NutritionTracker CV System](./Object_Detection_Project/)

A photo-based food classifier built with EfficientNet-B0, fine-tuned on Food-101 (101 classes, 75,750 training images). The system identifies a food item from a single image and returns the dish name plus estimated nutritional information (calories, protein, carbs, fat).

**Key result:** 86.27% Top-1 accuracy — cleared the ≥85% project target.

| Metric | Result |
|--------|--------|
| Top-1 Accuracy | **86.27%** ✅ |
| Architecture | EfficientNet-B0 (ImageNet → Food-101) |
| Training | Two-phase fine-tuning (15 epochs total) |
| Inference Speed | ~0.3 sec on T4 GPU |
| Classes | 101 food categories |

---

## Skills Demonstrated

- Transfer learning with pre-trained CNNs (EfficientNet-B0)
- Two-phase fine-tuning strategy (frozen backbone → full fine-tune)
- Data augmentation pipeline (RandomResizedCrop, ColorJitter, RandomRotation)
- Model evaluation: confusion matrix, per-class F1, classification report
- Top-K inference with nutrition lookup integration
- Google Colab + T4 GPU training workflow
