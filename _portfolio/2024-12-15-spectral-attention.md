---
title: "Spectral Band Attention Networks (SBAM)"
excerpt: "Novel architecture for Hyperspectral Band Selection achieving 95% accuracy. <br/><img src='images/spectral_attention/band_attention.png'>"
collection: portfolio
date: 2024-12-15
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Research](https://img.shields.io/badge/Research-Accepted-success?style=for-the-badge)

### 📄 Abstract
Classifying wheat seeds into 96 varieties using RGB and Hyperspectral data. [cite_start]While standard models like DenseNet-121 and ResNet-50 achieved ~78% on RGB, Hyperspectral data offered deeper insights[cite: 18]. [cite_start]This paper has been **accepted** for publication[cite: 21].

### 🔬 Key Innovation: SBAM
I developed a **Spectral Band Attention Module (SBAM)**. Instead of treating all bands equally, this module:
1.  [cite_start]**Ranks Bands:** Identifies which spectral bands contribute most to classifier accuracy[cite: 19].
2.  **Attention Mechanism:** Selectively amplifies features from high-contribution bands.

### 📊 Results
* [cite_start]**Base Accuracy:** 87% using SBAM on Hyperspectral images[cite: 19].
* [cite_start]**Ensemble Accuracy:** **95%** achieved by employing a Regression-based Ensemble (SVM) to combine model predictions[cite: 20].

### 🔗 Links
* [**Read the Paper**](#) * [**GitHub Repository**](#) ---

### 📸 Visual Library
*Model architecture diagrams, confusion matrices, and spectral heatmaps.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/spectral_attention' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Spectral Research" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>