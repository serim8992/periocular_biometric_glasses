# RockSiN: Robust Periocular Recognition under Glasses

RockSiN is a deep learning–based periocular recognition framework designed for robust verification,  
particularly effective under appearance variations such as glasses and Near-Infrared (NIR) imaging.

The proposed system adopts a Siamese architecture with explicit difference feature learning,  
enhancing discriminative capability between periocular image pairs.

> ⚠️ Note: Full implementation and datasets are maintained in a private laboratory repository due to institutional policy.  
> This public repository provides an overview of the architecture and experimental configuration.

---

## 🚀 Key Features

- **Siamese Architecture**  
  Dual-branch feature extraction for pairwise periocular matching.

- **Difference Feature Learning**  
  Explicit modeling of feature differences to improve verification robustness.

- **Flexible Backbone Networks**
  - MobileNetV3 (lightweight & efficient)
  - ResNet18 (strong baseline)
  - SHViT (Single-Head Vision Transformer)

- **Domain Robustness**
  Designed to handle glasses-induced domain shift and NIR appearance variation.

- **Configurable Training Pipeline**
  Modular design with command-line configuration.

---

## 🧠 Method Overview

RockSiN extracts embeddings from paired periocular images using shared-weight backbones.  
The resulting feature vectors are combined through difference learning and passed to a metric head  
for similarity estimation.

Main components:

- Feature Extractor (CNN / ViT backbone)
- Siamese Pair Encoding
- Difference Feature Module
- Metric Learning Head

This structure enables robust representation learning under cross-domain conditions.

---

## 🛠 Installation

```bash
git clone https://github.com/serim8992/RockSiN.git
cd RockSiN

pip install torch torchvision numpy opencv-python tqdm scikit-learn matplotlib
