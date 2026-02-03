# RockSiN: Robust Periocular Recognition under Glasses

RockSiN is a deep learning-based periocular recognition framework designed for robust verification,  
particularly effective under appearance variations such as glasses and Near-Infrared (NIR) imaging.

It adopts a Siamese architecture with explicit difference feature learning to enhance discriminative power  
for periocular pair matching.

> ⚠️ Note: Full implementation and datasets are maintained in a private laboratory repository due to institutional policy.  
> This public repository provides an overview of the method and experimental configuration.

---

## 🚀 Key Features

- **Siamese Architecture**: Dual-branch feature extraction for pairwise periocular matching.
- **Difference Feature Learning**: Explicit modeling of feature differences for improved discrimination.
- **Flexible Backbones**: MobileNetV3 / ResNet18 / SHViT.
- **Domain Robustness**: Designed for glasses-induced domain shift and NIR appearance variation.
- **Easy Configuration**: Command-line configurable pipeline.

---

## 🧠 Method Overview

RockSiN extracts embeddings from paired periocular images using shared-weight backbones.  
Feature vectors are combined via difference learning and passed to a metric head for similarity estimation.

Main components:

- Backbone Feature Extractor (CNN / ViT)
- Siamese Pair Encoding
- Difference Feature Module
- Metric Learning Head

---

## 🛠 Installation

```bash
git clone https://github.com/serim8992/RockSiN.git
cd RockSiN
pip install torch torchvision numpy opencv-python tqdm scikit-learn matplotlib
```

---

## 🏃 Usage (Example)

```bash
# ArcFace training
python main.py --mode arcface

# Contrastive learning
python main.py --mode contrastive

# Contrastive + Linear Probing
python main.py --mode contrastive_linear_probing
```

### Key Arguments

| Argument | Description | Default |
|---------|-------------|---------|
| --model_name | mobilenetv3, resnet18, shvit_s2 | mobilenetv3 |
| --data_dir | Dataset path | ./periocular_data |
| --epochs | Training epochs | 10 |
| --batch_size | Batch size | 32 |
| --lr | Learning rate | 0.0001 |
| --fold | Cross-validation fold | 1 |

---

## 📂 Project Structure

```
periocular_biometric_glasses/
├── data/
├── models/
├── training/
├── tools/
├── notebooks/
└── main.py
```

---

## 📄 Paper

RockSiN: Robust Cross-domain Siamese Network for Periocular Biometrics
(Currently under review)

---

## 👤 Maintainer

Selim Jeong  
Sangmyung University PRLab

---

⭐ If you find this project useful, a star is always appreciated.
```
