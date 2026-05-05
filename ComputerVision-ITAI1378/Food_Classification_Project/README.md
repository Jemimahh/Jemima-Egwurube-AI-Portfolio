# Food Classification — NutritionTracker CV System

**Course:** ITAI 1378 | **Author:** Jemima Egwurube | **Term:** Spring 2026  
**GitHub:** [Jemima-Egwurube-AI-Portfolio](https://github.com/Jemimahh/Jemima-Egwurube-AI-Portfolio)

---

## Project Summary

A single-image food classifier that identifies a food item from a photo and returns its name plus estimated nutritional information (calories, protein, carbs, fat). Built with EfficientNet-B0 fine-tuned on the Food-101 dataset using a two-phase transfer learning strategy.

**Pipeline:**
```
Photo input → Resize & Normalize (224×224) → EfficientNet-B0 → Top-3 Predictions → Nutrition Lookup → Result
```

---

## Results

| Metric | Target | Achieved |
|--------|--------|----------|
| Top-1 Accuracy | ≥ 85% | **86.27% ✅** |
| Inference Speed | < 2 sec | ~0.3 sec (T4 GPU) |
| Training Samples | — | 75,750 |
| Val Samples | — | 25,250 |
| Food Classes | — | 101 |

### Training History

| Phase | Epochs | Val Accuracy |
|-------|--------|--------------|
| Phase 1 — frozen backbone | 5 | 53.05% → 58.37% |
| Phase 2 — full fine-tune  | 10 | 78.14% → **86.27%** |

### Top / Hardest Classes

| Class | F1 | Notes |
|-------|----|-------|
| bibimbap | 0.949 | Distinct bowl + geometric color layout |
| cannoli | 0.933 | Unique tubular shape |
| churros | 0.928 | Clear elongated silhouette |
| apple_pie | 0.684 | Confused with bread_pudding — brown baked cluster |
| bread_pudding | 0.708 | Visually similar to other baked dishes |
| chocolate_mousse | 0.722 | Similar to other dark chocolate desserts |

See [`results/performance_metrics.png`](./results/performance_metrics.png) for training curves and full per-class F1 chart.

---

## Files

```
Object_Detection_Project/
├── Object_Detection.ipynb        ← full training & inference notebook (executed)
├── README.md                     ← this file
└── results/
    ├── performance_metrics.png   ← training curves + per-class F1 bar chart
    └── detected_images/          ← inference output panels (add after running)
```

---

## How to Run

1. Open `Object_Detection.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Set runtime to **GPU (T4)**
3. Run all cells — Food-101 downloads automatically (~5 GB), no Kaggle key needed
4. Upload your own food photos in the final inference cell
5. Save inference output panels to `results/detected_images/`

---

## Model & Training Details

**Architecture:** EfficientNet-B0 (ImageNet pre-trained) → `Dropout(0.3) → Linear(1280, 101)`  
**Framework:** PyTorch + torchvision  
**Dataset:** torchvision `datasets.Food101` — 75,750 train / 25,250 val

**Training config:**
- Phase 1: Adam lr=1e-3, CosineAnnealingLR, backbone frozen, 5 epochs
- Phase 2: Adam lr=1e-4 wd=1e-4, CosineAnnealingLR eta_min=1e-6, all layers, 10 epochs
- Loss: CrossEntropyLoss with label_smoothing=0.1

**Data augmentation (train only):**
- RandomResizedCrop(224, scale=0.7–1.0)
- RandomHorizontalFlip
- ColorJitter(brightness=0.3, contrast=0.3, saturation=0.2)
- RandomRotation(15°)
- ImageNet normalization

---

## Key Learnings

The biggest accuracy gain (58% → 78% in a single epoch) came from unfreezing the backbone in Phase 2 — not from any optimizer tuning. This illustrates that for transfer learning on visual tasks, **feature specialization matters more than hyperparameter search**.

The hardest class cluster (apple_pie, bread_pudding, chocolate_cake) shows a genuine visual ambiguity at 224×224 resolution — these are structurally identical brown baked dishes. Mitigations would include targeted data augmentation or test-time augmentation (TTA).

---

## References

- EfficientNet: Tan & Le, 2019 — https://arxiv.org/abs/1905.11946
- Food-101: Bossard et al., 2014 — https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/
- torchvision EfficientNet: https://pytorch.org/vision/stable/models/efficientnet.html
- Nutrition values: USDA FoodData Central estimates
