---
title: "AI Agent 007: Tooling up for Success"
excerpt: "Self-reflective ReAct agent for autonomous tool allocation and parameter extraction. <br/><img src='../images/agent007/certificate.png'  style='height: 200px; width: auto;'><br/>"
collection: portfolio
date: 2023-12-20
---

![LangChain](https://img.shields.io/badge/LangChain-ReAct-green?style=for-the-badge)
![GPT-4](https://img.shields.io/badge/GPT--4-OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### 🏆 Achievement
[cite_start]**Secured Rank 3** in the *Tooling up for Success* challenge at **Inter-IIT Techfest 2023**[cite: 47]. [cite_start]Competing in the DevRev AI Agent Track against top Indian technical institutes, our solution excelled in autonomous tool management[cite: 47].

### 🤖 The Challenge
[cite_start]The objective was to build a "query-aware" agent capable of intelligently allocating tasks to specific tools and reviewing their outputs without human intervention[cite: 42].

### 🧠 Architecture: Self-Reflective ReAct
[cite_start]I implemented a **ReAct (Reason + Act) style agent** that operates in a loop[cite: 44]:
1.  **Thought:** The agent analyzes the user query to understand intent.
2.  [cite_start]**Tool Allocation:** It autonomously selects the correct tool for the job (e.g., parameter extraction, API calls)[cite: 44].
3.  [cite_start]**Reflection:** The agent reviews the tool's output to ensure accuracy before generating the final response[cite: 42].
4.  [cite_start]**Data Curation:** We curated a custom dataset based on specific tool descriptions to fine-tune the agent's decision-making capabilities[cite: 44].

### 🔗 Links
* [**View Code on GitHub**](#) * [**Competition Leaderboard**](#) ---

### 📸 Visual Library
*Agent decision flowcharts, terminal logs of "Thought-Act-Observation" loops.*

<div class="gallery-container">
    {% for file in site.static_files %}
      {% if file.path contains 'images/agent007' %}
        <img src="{{ site.baseurl }}{{ file.path }}" class="gallery-img" alt="AI Agent Project" />
      {% endif %}
    {% endfor %}
</div>

<style>
  .gallery-container { display: flex; justify-content: center; flex-wrap: wrap; gap: 15px; padding: 20px; background: #f4f4f4; border-radius: 10px; }
  .gallery-img { height: 200px; width: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; }
  .gallery-img:hover { transform: scale(1.03); }
</style>