---
title: "Spectral Band Attention Networks: Efficient Multi-Feature Fusion"
excerpt: "<b>Published in Springer.</b> <br> Novel Attention-based Band Selection achieving 95.75% accuracy on 96-class Hyperspectral dataset. <br/><img src='../images/spectral_attention/band_attention.png' style='height: 200px; width: auto; margin-top: 10px;'><br/>"
collection: portfolio
date: 2024-12-15
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Springer](https://img.shields.io/badge/Springer-Published-006699?style=for-the-badge&logo=springer&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### 📄 Abstract & Problem Statement
Rapid, nondestructive seed variety identification is critical for agricultural efficiency. While **Hyperspectral Imaging (HSI)** offers rich spectral data (900-1700 nm), it suffers from the "curse of dimensionality"—redundant bands lead to overfitting, while low spatial resolution makes separating individual seeds difficult. 

This research addresses these challenges by proposing a **Spectral Band Attention Network (SBAN)** to intelligently select informative bands and a multi-modal pipeline to fuse spectral and spatial features.

### 🔬 Methodology: Attention & Fusion
The proposed architecture integrates feature extraction and dimensionality reduction into a unified pipeline:

#### 1. Spectral Band Attention Network (SBAN)
To overcome high dimensionality, a novel attention mechanism was developed that:
* **Ranks Channels:** Dynamically calculates the importance weight of each spectral band.
* **Filters Redundancy:** Identified **25 optimal bands** out of the full spectrum, discarding noise while retaining discriminative features.
* **Outperforms Baselines:** Demonstrated superior selection compared to Sparse Band Attention, PCA-loading, and Triplet-attention methods.

#### 2. Multi-Modal Ensemble Framework
To leverage both spatial (RGB) and spectral (HSI) details, a stacked ensemble model was constructed:
* **Backbones:** Utilized four deep CNNs—**Customized DenseNet, GoogLeNet, ResNet34, and DenseNet121**.
* **Fusion Strategy:** Extracted features from both modalities are concatenated and passed to a **Support Vector Machine (SVM)** classifier for the final prediction.

### 📊 Results
Tested on a massive custom dataset of **96 Indian wheat varieties**:
* **Accuracy:** Achieved **95.75%** test accuracy using the Ensemble + SBAN approach.
* **Efficiency:** Maintained high performance using only **25 selected bands**, significantly reducing computational overhead compared to full-spectrum analysis.

### 🔗 Links
* [**Read the Paper (Springer)**](https://link.springer.com/article/10.1007/s10921-025-01215-8)
* [**View Code on GitHub**](https://github.com/Sar2580P/Spectral-Band-Attention-Networks-for-Efficient-Multi-Feature-Fusion-in-Hyperspectral-and-RGB-Data)

---

### 📸 Visual Library
*Network architecture, spectral band selection heatmaps, and confusion matrices for 96-class classification.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/spectral_attention' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Spectral Research" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; margin-top: 20px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>