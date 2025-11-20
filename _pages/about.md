---
permalink: /
title: "👋 Hello there, I'm  SARVAGYA!"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<!-- LAYOUT: TWO COLUMN INTRO TABLE -->

<table border="0" width="100%">
<tr>

<!-- LEFT COLUMN: THE INTRO -->

<td width="65%" valign="center">
<!-- <h1>👋 Hi there, I'm Sarvagya!</h1> -->




<!-- BIO SECTION -->

<h3>
🤖 I'm an AI Researcher exploring the intersection of <strong>Offline RL</strong> and <strong>Generative AI</strong>.
</h3>

<h3>
🚀 Currently working as an SDE-1 at <strong>Avathon</strong>, building scalable distributed systems.
</h3>

<h3>
🎓 I'm a recent graduate from <strong>IIT Roorkee</strong> (Class of '25).
</h3>

<h3>
🏆 <strong>Global Rank 3</strong> in the NeurIPS 2025 Pokemon AI Competition (Game RL).
</h3>

<!-- RIGHT COLUMN: THE IMAGE -->

<td width="35%" valign="center" align="center">
<!--
NOTE: The filename has a space, so we use '%20' to encode it.
Ensure 'formal_photo_short copy.jpg' exists inside the 'images' folder.
-->
<img src="{{ site.baseurl }}/images/HOME-PAGE-INTRO.png" width="250" alt="Mr Porwal" style="border-radius: 15px;" />
</td>

</tr>
</table>


<h3>🚀 Technical Domain Expertise</h3>

<table border="0" width="100%" cellspacing="15" cellpadding="0" style="border-collapse: separate; border-spacing: 15px;">

<tr>

<td width="50%" valign="top" style="background-color: #fff1f0; border: 1px solid #ffa39e; border-radius: 15px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0; color: #cf1322;">🎮 Reinforcement Learning</h3>
    <ul style="padding-left: 20px; color: #262626; margin-bottom: 0;">
        <li><strong>Algorithm:</strong> Adaptive Hedge ensemble, TD-error selection.</li>
        <li><strong>Policy:</strong> Actor-Critic with Offline Reinforcement Learning[cite: 26].</li>
        <li><strong>Win:</strong> Global Rank 3, NeurIPS 2025[cite: 28].</li>
    </ul>
</td>

<td width="50%" valign="top" style="background-color: #e6f7ff; border: 1px solid #91d5ff; border-radius: 15px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0; color: #0050b3;">👁️ Computer Vision Research</h3>
    <ul style="padding-left: 20px; color: #262626; margin-bottom: 0;">
        <li><strong>Paper:</strong> Spectral Band Attention Networks (Accepted).</li>
        <li><strong>Method:</strong> Band selection via attention-based ranking[cite: 19].</li>
        <li><strong>Result:</strong> 95% Accuracy on Hyperspectral data[cite: 20].</li>
    </ul>
</td>

</tr>

<tr>

<td width="50%" valign="top" style="background-color: #f9f0ff; border: 1px solid #d3adf7; border-radius: 15px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0; color: #722ed1;">✨ GenAI Research & Search</h3>
    <ul style="padding-left: 20px; color: #262626; margin-bottom: 0;">
        <li><strong>Research:</strong> Smoothed Energy Guidance (NeurIPS Reproducibility)[cite: 8, 11].</li>
        <li><strong>Deep Learning:</strong> Latent trajectory tracking, Gradient Entropy.</li>
        <li><strong>RAG:</strong> Graph-based agents, cyclic metadata storage[cite: 32, 33].</li>
    </ul>
</td>

<td width="50%" valign="top" style="background-color: #f6ffed; border: 1px solid #b7eb8f; border-radius: 15px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0; color: #389e0d;">💼 Experience & Systems</h3>
    <ul style="padding-left: 20px; color: #262626; margin-bottom: 0;">
        <li><strong>Avathon:</strong> Distributed Celery pipelines, Microservices[cite: 53].</li>
        <li><strong>Internship:</strong> Enterprise RAG, AWS Vector Search[cite: 59].</li>
        <li><strong>Scale:</strong> Optimized CRUD for millions of docs[cite: 60].</li>
    </ul>
</td>

</tr>
</table>



<h3>📸 Project Gallery</h3>

<style>
  .gallery-container {
    width: 100%;
    overflow: hidden;
    white-space: nowrap;
    position: relative;
    background: #f9f9f9; /* Optional background color */
    border-radius: 15px; /* Curved edges for container */
    padding: 10px 0;
  }

  .gallery-track {
    display: inline-block;
    animation: scroll 40s linear infinite; /* Adjust speed (40s) as needed */
  }

  .gallery-img {
    height: 180px; /* Fixed height for uniformity */
    width: auto;
    margin: 0 10px;
    border-radius: 10px; /* Curved edges for images */
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    vertical-align: middle;
    transition: transform 0.3s;
  }

  .gallery-img:hover {
    transform: scale(1.05); /* Slight zoom on hover */
    cursor: pointer;
  }

  /* The animation keyframes */
  @keyframes scroll {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }
  
  /* Pause scrolling on hover for better UX */
  .gallery-container:hover .gallery-track {
    animation-play-state: paused;
  }
</style>

<div class="gallery-container">
  <div class="gallery-track">
    
    {% for file in site.static_files %}
      {% if file.path contains 'images/gallery' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Project Image" />
      {% endif %}
    {% endfor %}

    {% for file in site.static_files %}
      {% if file.path contains 'images/gallery' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Project Image" />
      {% endif %}
    {% endfor %}

  </div>
</div>