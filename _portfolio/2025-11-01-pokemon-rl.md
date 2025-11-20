---
title: "Global Rank 3: NeurIPS 2025 Pokemon AI Competition"
excerpt: "Reinforcement Learning agent with Adaptive Hedge Ensemble.<br/><img src='../images/pokemon_AI/pokemon_poster.png' style='height: 90px; width: auto;'><br/>"
collection: portfolio
date: 2025-11-01
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![RL](https://img.shields.io/badge/Offline_RL-000000?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### 🏆 Achievement
**Secured Global Rank 3** in Track-1 with a policy ELO rating of **1793**, demonstrating superior generalization in unseen competitive scenarios.

### ⚔️ The Challenge
The goal was to create an AI agent capable of playing competitive Pokemon battles. The challenge involved handling a vast action space, hidden information, and stochastic game mechanics.

### 🧠 Methodology
We approached this as an **Imitation Learning** and **Offline Reinforcement Learning** problem.

1.  **Actor-Critic Policy:** Trained on game replay datasets to learn optimal move selection.
2.  **Exploration Enhancement:** Enhanced standard Behavior Cloning with exploration mechanisms to prevent the agent from getting stuck in local optima.
3.  **Adaptive Ensemble (The Winning Edge):** We engineered a policy ensemble to mitigate high action-entropy. The system dynamically selected confident agents based on **TD (Temporal Difference) error**, allowing the bot to handle less explored scenarios robustly.

### 🔗 Links
* [**View Code on GitHub**](#) * [**Competition Leaderboard**](#) ---

### 📸 Visual Library
*Gameplay screenshots, reward curves, and training logs.*

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/pokemon_AI' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Pokemon RL Project" />
      {% endif %}
    {% endfor %}
</div>