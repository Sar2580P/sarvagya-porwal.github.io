---
title: "Global Rank 3: NeurIPS 2025 Pokemon AI Competition"
excerpt: "<b>NeurIPS 2025 Global Rank 3.</b> <br> Hybrid Imitation-RL agent with Adaptive Hedge Ensemble and Q-filtered exploration.<br/><img src='../images/pokemon_AI/pokemon_poster.png' style='height: 200px; width: auto; margin-top: 10px;'><br/>"
collection: portfolio
date: 2025-11-01
---

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![RL](https://img.shields.io/badge/Offline_RL-Imitation-000000?style=for-the-badge)

### 🏆 Achievement
**Secured Global Rank 3** (Team: *srsk-1729*) in Track-1 with a policy ELO rating of **1793**. Our agent demonstrated superior generalization in unseen competitive scenarios, outperforming standard baselines in the official NeurIPS 2025 benchmark.

### ⚔️ The Challenge
The goal was to create an AI agent capable of playing competitive Pokemon battles. The challenge involves a **Partially Observable Markov Decision Process (POMDP)** characterized by a vast action space, hidden information (opponent moves/stats), and highly stochastic game mechanics.

### 🧠 Methodology
We approached this as a hybrid **Imitation Learning** and **Offline Reinforcement Learning** problem.

#### 1. Imitation Learning with Exploration
Instead of standard Behavior Cloning, we implemented a weighted imitation objective regularized by a Q-value function. This allows the agent to mimic expert moves while exploring high-reward actions that the expert might have missed.

**The Actor Loss Function:**
$$\mathcal{L}_{\text{Actor}} = \mathbb{E}_{\tau \sim \mathcal{D}} \left[ \frac{1}{T} \sum_{t=0}^{T} \left( -w(h_t, a_t) \log \pi(a_t \mid h_t) - \lambda \mathbb{E}_{a \sim \pi(\cdot|h_t)} [Q(h_t, a)] \right) \right]$$

* **First Term (Imitation):** `-w(h`<sub>`t`</sub>`, a`<sub>`t`</sub>`) log &pi;(a`<sub>`t`</sub>` | h`<sub>`t`</sub>`)` maximizes the likelihood of expert actions, weighted by their relevance *w*.
* **Second Term (Exploration):** `-&lambda; E [Q(h`<sub>`t`</sub>`, a)]` acts as an entropy-regularized exploration bonus, pushing the policy *&pi;* towards actions with higher estimated Q-values, even if they deviate slightly from the dataset.

#### 2. Adaptive Hedge Ensemble (The Winning Edge)
To mitigate high action-entropy in ambiguous states, we engineered a policy ensemble. The system dynamically selected the most confident agent based on **TD (Temporal Difference) error**, allowing the bot to handle less explored scenarios robustly by switching policies when prediction error spiked.

### 🔗 Links
* [**View Code on GitHub**](https://github.com/Sar2580P/Pokemon-Challenge-track1)
* [**Competition Leaderboard**](https://pokeagent.github.io/leaderboard.html)

---

### 📸 Visual Library
*Gameplay screenshots, reward curves, and training logs.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/pokemon_AI' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="Pokemon RL Project" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; margin-top: 20px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>