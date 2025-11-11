# Explainability Simulator for Autonomous Vehicles

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

> A machine learning project investigating how different AI explanation styles affect human trust and comprehension in autonomous vehicle decision-making scenarios.

---

## 🎯 Project Overview

This project investigates how different AI explanation styles affect human trust and comprehension in autonomous vehicle decision-making scenarios. Using natural language processing and sentiment analysis, the simulator evaluates which communication strategies build passenger confidence in safety-critical driving situations.

---

## 🔬 Research Motivation

Autonomous vehicles must not only make correct decisions but also communicate those decisions in ways humans can understand and trust. As self-driving cars become mainstream, the gap between AI decision-making and human comprehension poses significant challenges to user acceptance. 

**This research addresses the critical question:** *How should autonomous vehicles explain their actions to maximize passenger trust across different risk scenarios?*

Understanding optimal explanation design is essential for:
- **Safety**: Clear communication during emergencies reduces panic and improves outcomes
- **Adoption**: Trust is the primary barrier to autonomous vehicle acceptance
- **User Experience**: Passengers need reassurance that the system is reliable and transparent

---

## 🛠️ Technologies Used

### Machine Learning Models
- **DistilBERT** (`distilbert-base-uncased-finetuned-sst-2-english`)
  - Lightweight transformer model (~67M parameters)
  - Sentiment analysis and text understanding
  - Optimized for Google Colab free tier
 
## 🔍 Key Results

### Trust Score Rankings (0-1 scale)

| Rank | Explanation Style | Avg Trust Score | Std Deviation |
|------|------------------|-----------------|---------------|
| 🥇 1 | **Emotional**    | **0.949**       | ±0.062        |
| 🥈 2 | Technical        | 0.736           | ±0.149        |
| 🥉 3 | Factual          | 0.650           | ±0.120        |
| 4    | Minimal          | 0.498           | ±0.193        |

### Major Findings

✅ **Emotional explanations generate 91% higher trust** than minimal explanations

✅ **Risk-appropriate communication matters**: Emotional style performs best in high-risk scenarios (0.902 trust score)

✅ **Length ≠ Trust**: Longer factual explanations reduce trust (-0.466 correlation), while emotional style maintains trust regardless of length

✅ **Consistency**: Emotional explanations show lowest variance (±0.062), indicating reliable trust across diverse scenarios

### Context-Specific Performance

| Risk Level | Best Style | Trust Score |
|------------|------------|-------------|
| High       | Emotional  | 0.902       |
| Medium     | Emotional  | 0.957       |
| Low        | Emotional  | 0.979       |

### Explanation Length Correlations

| Style     | Length-Trust Correlation | Interpretation                    |
|-----------|--------------------------|-----------------------------------|
| Factual   | -0.466                   | More words = less trust           |
| Emotional | -0.007                   | Length doesn't affect trust       |
| Technical | +0.183                   | More detail = more trust          |
| Minimal   | +0.065                   | Slightly positive (brief by design)|

---
