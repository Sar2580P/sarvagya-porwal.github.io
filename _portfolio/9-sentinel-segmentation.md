---
title: "Sentinel-2 Field Delineation"
excerpt: "High-precision agricultural field segmentation using Hyperspectral Imagery and Spectral Indices. <br/><img src='../images/sentinel_project/output.png' style='height: 200px; width: auto; margin-top: 10px;'><br/>"
collection: portfolio
date: 2024-08-01
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Remote Sensing](https://img.shields.io/badge/Remote%20Sensing-Indices-success?style=for-the-badge)
![Segmentation](https://img.shields.io/badge/CV-Segmentation-blue?style=for-the-badge)

### 🌍 The Mission
To engineer a robust field delineation pipeline capable of accurately identifying agricultural boundaries using high-resolution multi-channel satellite imagery provided by Solafune. 
* **The Challenge:** The model had to resolve dense clusters of **100+ distinct farms** within a single satellite patch, requiring high instance separation capabilities.

### 🌿 Spectral Feature Engineering
To augment the raw satellite bands, I computed pixel-wise spectral indices to feed the model explicit physical properties of the terrain. This "physics-informed" approach significantly improved boundary detection:

* **NDVI (Normalized Difference Vegetation Index):** * *Bands:* B8 (NIR) & B4 (Red).
    * *Purpose:* Highlights the density of **Green Vegetation**, crucial for separating crops from soil.
* **NDWI (Normalized Difference Water Index):**
    * *Bands:* B4 (Red) & B11 (SWIR).
    * *Purpose:* Detects **Surface Water**, helping to distinguish irrigation channels from fields.
* **NDSI (Normalized Difference Snow Index):**
    * *Bands:* B3 (Green) & B11 (SWIR).
    * *Purpose:* Maps the extent of **Snow Cover** (or highly reflective surfaces) to prevent false positives.
* **GSI (Grain Size Index):**
    * *Bands:* B4 (Red), B2 (Blue), & B3 (Green).
    * *Purpose:* Identifies areas with advanced **Desertification**, aiding in the exclusion of non-arable land.

### 🛰️ Architecture & Backbones
Implemented and benchmarked a diverse suite of semantic segmentation models to maximize feature extraction:
* **Unet:** The standard baseline for biomedical and satellite segmentation.
* **Unet++:** Utilized nested dense skip pathways to reduce the semantic gap.
* **FPN (Feature Pyramid Networks):** Implemented to handle multi-scale detection across varying resolutions.
* **DeepLabv3:** Leveraged atrous (dilated) convolutions to capture wider context without losing spatial resolution.

### 📐 Mathematical Framework: Loss & Metrics
To handle the class imbalance between field boundaries and land area, I engineered a **Joint Total Loss** function:

**1. The Objective Function**
$$L_{Total} = 0.9 \times L_{Focal} + 0.1 \times L_{Jaccard}$$

**2. Focal Loss ($L_{Focal}$)**
Focuses learning on "hard" examples (sparse boundaries) by down-weighting easy negatives:
$$L_{Focal}(p_t) = - (1 - p_t)^\gamma \log(p_t)$$

**3. Jaccard Loss ($L_{Jaccard}$) & IoU**
Directly optimizes the Intersection over Union metric:
$$IoU = \frac{|Y \cap \hat{Y}|}{|Y \cup \hat{Y}|} \quad \Rightarrow \quad L_{Jaccard} = 1 - IoU$$

### ⚙️ The Pipeline
1.  **Data Prep:** Precise annotation polygons were extracted from raw satellite patches using **OpenCV**.
2.  **Ensemble Strategy:** Designed a stacking ensemble that aggregated prediction masks from the fine-tuned models. This "wisdom of crowds" approach smoothed out edge-case errors.

### 📉 Training Dynamics
The ensemble model demonstrated excellent convergence with strong generalization.
* **Final Validation Focal Loss:** Converged to **0.052**.
* **Final Validation Jaccard Loss:** Stabilized at **0.447**.
* **Total Validation Loss:** Achieved a final value of **0.091**.

### 🎯 Impact
* **Metric:** Achieved a segmentation **Intersection over Union (IoU) of 0.96**.
* **Result:** Created a high-fidelity mapping tool suitable for automated agricultural analysis.

### 🔗 Links
* [**View Code on GitHub**](https://github.com/Sar2580P/Fin7X8Ph4Ai2)

---

### 📸 Visual Library
*Segmentation masks, satellite patches, and Training Loss curves.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/sentinel_project' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Sentinel Project" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; margin-top: 20px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>