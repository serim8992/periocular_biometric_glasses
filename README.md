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
