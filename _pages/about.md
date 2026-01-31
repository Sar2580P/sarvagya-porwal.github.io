---
permalink: /
title: "👋 Hello there, I'm  SARVAGYA!!!"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<!-- LAYOUT: TWO COLUMN INTRO -->
<style>
  .intro-container {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 30px;
    margin-bottom: 20px;
  }
  
  .intro-text {
    flex: 1;
    min-width: 280px;
  }
  
  .intro-image {
    flex-shrink: 0;
  }
  
  .intro-image img {
    max-width: 250px;
    border-radius: 15px;
  }
  
  @media (max-width: 600px) {
    .intro-container {
      flex-direction: column-reverse;
      text-align: center;
    }
    
    .intro-image img {
      max-width: 200px;
    }
  }
</style>

<div class="intro-container">
  <div class="intro-text" style="font-family: sans-serif; font-size: 16px; line-height: 2;">
    <div>🤖 <strong>Research Interest:</strong> RL &times; Generative AI</div>
    <div>🚀 <strong>Current Role:</strong> SDE-1 @ <strong>Avathon</strong></div>
    <div>🎓 <strong>Education:</strong> B.Tech, <strong>IIT Roorkee</strong> '25</div>
    <div>🏆 <strong>Achievement:</strong> Global Rank #3 @ <strong>NeurIPS Competition 2025</strong> (Game AI)</div>
  </div>
  <div class="intro-image">
    <img src="{{ site.baseurl }}/images/llama1.jpeg" alt="Mr Porwal" />
  </div>
</div>

<h3>🚀 Technical Domain Expertise</h3>

<style>
  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
    width: 100%;
  }
  
  @media (max-width: 768px) {
    .expertise-grid {
      grid-template-columns: 1fr;
    }
  }
  
  .expertise-card {
    border-radius: 15px;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  
  .expertise-card h4 {
    margin-top: 0;
    margin-bottom: 12px;
    font-size: 1.1em;
  }
  
  .expertise-card ul {
    padding-left: 20px;
    color: #262626;
    margin-bottom: 0;
  }
  
  .expertise-card li {
    margin-bottom: 8px;
  }
  
  .expertise-card li:last-child {
    margin-bottom: 0;
  }
</style>

<div class="expertise-grid">

<div class="expertise-card" style="background-color: #fff1f0; border: 1px solid #ffa39e;">
    <h4 style="color: #cf1322;">🎮 Reinforcement Learning</h4>
    <ul>
        <li><strong>Imitation Learning</strong> with exploration on Gen-1 Competitive Pokemon.</li>
        <li><strong>Adaptive Hedge Ensemble</strong> of policies using TD error to increase the state-action space coverage.</li>
        <li><strong>Rank-3</strong> in Competitive Pokemon AI in NeurIPS 2025 competition.</li>
    </ul>
</div>

<div class="expertise-card" style="background-color: #e6f7ff; border: 1px solid #91d5ff;">
    <h4 style="color: #0050b3;">👁️ Computer Vision Research</h4>
    <ul>
        <li>Proposed novel <strong>attention-based band selection</strong> technique for hyperspectral data (Published in Journal).</li>
        <li>Achieving <strong>on-par performance using just 15%</strong> of total bands (168).</li>
        <li><strong>Multi-modal pipeline</strong> for joint input of RGB + Hyperspectral data, achieving <strong>95% accuracy</strong> on wheat seed classification (96 classes).</li>
    </ul>
</div>

<div class="expertise-card" style="background-color: #f9f0ff; border: 1px solid #d3adf7;">
    <h4 style="color: #722ed1;">✨ GenAI Research & Search</h4>
    <ul>
        <li>Worked on reproducibility of <strong>Smoothed Energy Guidance</strong> (NeurIPS 2024) for improved quality generation in diffusion models.</li>
        <li>Proposed mathematically equivalent and <strong>computationally cheaper alternative</strong> smoothing techniques.</li>
        <li>Achieving even <strong>better FID & CLIP scores</strong> with proposed techniques (Paper under review).</li>
    </ul>
</div>

<div class="expertise-card" style="background-color: #f6ffed; border: 1px solid #b7eb8f;">
    <h4 style="color: #389e0d;">💼 Experience & Systems</h4>
    <ul>
        <li><strong>Avathon:</strong> Developing <strong>Neon</strong>, a proprietary Scala-based graph database for supply chains, implementing distributed semantic search across graph nodes.</li>
        <li><strong>Internship:</strong> Built an <strong>Enterprise RAG pipeline</strong> on AWS using Postgres vector-stores for high-performance information retrieval.</li>
        <li>Engineered critical <strong>Retriever, Re-ranker, and Caching</strong> components to maximize chatbot integration efficiency and scalability.</li>
    </ul>
</div>

</div>



<h3>📸 Project Gallery</h3>

<style>
  .gallery-container {
    display: flex;           /* aligns items in a row */
    justify-content: center; /* centers items horizontally */
    flex-wrap: wrap;         /* allows items to wrap if screen is small */
    gap: 20px;               /* space between images */
    padding: 20px;
    background: #f9f9f9;     /* light grey background */
    border-radius: 15px;     /* curved container edges */
    box-shadow: inset 0 0 10px rgba(0,0,0,0.05); /* subtle inner shadow */
  }

  .gallery-img {
    height: 220px;           /* Fixed height makes them uniform */
    width: auto;             /* Width adjusts automatically */
    border-radius: 10px;     /* curved image edges */
    box-shadow: 0 4px 8px rgba(0,0,0,0.1); /* nice shadow pop */
    transition: transform 0.3s ease;       /* smooth hover animation */
    cursor: pointer;
  }

  /* Interactive Hover Effect */
  .gallery-img:hover {
    transform: translateY(-5px) scale(1.02); /* lifts image slightly */
    box-shadow: 0 8px 15px rgba(0,0,0,0.15);
  }
</style>

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/gallery' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Project Image" />
      {% endif %}
    {% endfor %}
</div>