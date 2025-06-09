# Emotion-Cause Pair Extraction in Conversations

This repository presents a comparative study of different approaches to **Emotion-Cause Pair Extraction (ECPE)** in conversations. The task involves identifying emotions and their underlying causes from multi-turn dialogue data.

---

## Problem Statement

Traditional emotion detection often lacks context-awareness and causality understanding. This project aims to extract emotion-cause pairs from conversational text, a crucial step toward emotionally intelligent AI applications in chatbots, mental health tools, and social media analytics.

---

## Project Objectives

- Build end-to-end and transformer-based architectures for ECPE.
- Investigate prompt-tuning with pre-trained LLMs.
- Compare performance on standard ECPE metrics: precision, recall, and F1.
- Evaluate using a real-world conversation dataset (ECF).

---

## Dataset

We used the **Emotion-Cause-in-Friends (ECF)** dataset, derived from the *Friends* sitcom:

- 1,344 conversations
- 13,509 utterances
- 9,272 labeled emotion-cause pairs
- 6 basic emotions: joy, sadness, anger, disgust, fear, surprise


---

## Model Architectures

### 1. E2E-PExtE: End-to-End Pair Extraction Model

Hierarchical BiLSTM encoders for emotion and cause detection with shared auxiliary learning, followed by Cartesian pair prediction.

<p align="center">
  <img src="images/End-to-End Network.png" alt="E2E Architecture" width="700"/>
</p>

---

### 2. EmoBERTa + DeBERTa: Speaker-Aware Classification

Combines EmoBERTa for emotion detection and a transformer for cause identification. DeBERTa enhances final pair reasoning using QA-style prompt-tuning.

<p align="center">
  <img src="images/Architecture of the EmoBERTa-Based Approach.png" alt="EmoBERTa Architecture" width="700"/>
</p>

---

### 3. Prompt-Tuned LLMs (OPT-350M, LLaMA2, Vicuna)

Models are fine-tuned via formatted conversational prompts. Output parsing remains a challenge due to inconsistent generation formats.

<p align="center">
  <img src="images/Architecture used for Prompt-Tuning LMs.png" alt="Prompt Tuning Architecture" width="700"/>
</p>

---

