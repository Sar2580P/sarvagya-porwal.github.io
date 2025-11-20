---
title: "Sentinel-2 Field Delineation"
excerpt: "High-precision agricultural field segmentation using Hyperspectral Imagery. <br/><img src='../images/sentinel_project/output.png'  style='height: 200px; width: auto;'><br/>"
collection: portfolio
date: 2024-08-01
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Segmentation](https://img.shields.io/badge/CV-Segmentation-blue?style=for-the-badge)

### 🌍 The Mission
[cite_start]To engineer a robust field delineation pipeline capable of accurately identifying agricultural boundaries using high-resolution hyperspectral imagery provided by Solafune[cite: 39].

### 🛰️ Architecture & Models
I moved beyond standard segmentation by implementing and fine-tuning a suite of advanced architectures:
* **UNet++:** For capturing nested sub-features in complex field boundaries.
* **FPN (Feature Pyramid Networks):** To handle multi-scale detection of fields.
* [cite_start]**Mask-RCNN:** For instance-level segmentation of distinct plots[cite: 39].

### ⚙️ The Pipeline
1.  [cite_start]**Data Prep:** Extracted precise annotation polygons from raw patches using **OpenCV**[cite: 40].
2.  **Ensemble Strategy:** Designed a stacking ensemble that aggregated prediction masks from the fine-tuned models. [cite_start]This "wisdom of crowds" approach smoothed out edge-case errors from individual architectures[cite: 40].

### 🎯 Impact
* [cite_start]**Metric:** Achieved a segmentation **Intersection over Union (IoU) of 0.96**[cite: 40].
* **Result:** Created a high-fidelity mapping tool suitable for automated agricultural analysis.

### 🔗 Links
* [**View Code on GitHub**](#) * [**Project Demo**](#) ---

### 📸 Visual Library
*Segmentation masks, satellite patches, and IoU heatmaps.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/sentinel_project' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Sentinel Project" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>