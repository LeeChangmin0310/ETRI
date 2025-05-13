# Emotion Recognition using ECG and Micro-Expressions (ETRI Project)

A multi-modal machine learning framework for emotion recognition using ECG-derived cardiac features and micro facial expressions. This repository is developed as part of the ETRI Emotion Intelligence research project.

---

## 📌 Overview

This project aims to classify emotional states using:

- **Cardiac information** derived from raw ECG signals
- **Micro facial expressions** extracted from videos
- **Multi-modal fusion** of both modalities

In addition, we evaluate how **Emotional Intelligence (EI)** differences influence model performance.

---

## 🎯 Emotion Labels

We use a 4-class label system based on arousal and valence:

| Code  | Description                  |
|-------|------------------------------|
| HAHV  | High Arousal, High Valence   |
| HALV  | High Arousal, Low Valence    |
| LAHV  | Low Arousal, High Valence    |
| LALV  | Low Arousal, Low Valence     |

---

## 📁 Data

All datasets used in this repository are collected under the ETRI emotion recognition study. The data includes:

- `ECG`: Preprocessed signal features (e.g., HRV, time-domain)
- `Facial`: Micro-expression features extracted via video analysis
- `Labels`: Emotion class for each trial
- `EI Scores`: Subject-wise emotional intelligence scores

> ❗ rPPG is **not** used in this project.

---

## 🧠 EI-based Performance Analysis

Subjects are grouped into **High-EI** and **Low-EI** groups. We analyze:

- Accuracy differences by EI level
- Signal stability and feature distribution
- Physiological vs. behavioral expression gaps

---

## 🔬 Experiments (via Jupyter Notebooks)

This project is developed in Python with Jupyter notebooks.

| Notebook                                 | Description                                |
|------------------------------------------|--------------------------------------------|
| `1_preprocessing.ipynb`                  | ECG preprocessing and feature extraction   |
| `2_facial_features.ipynb`                | Extract micro-expression features          |
| `3_ecg_classification.ipynb`             | ECG-only classification                    |
| `4_facial_classification.ipynb`          | Facial-only classification                 |
| `5_fusion_classification.ipynb`          | ECG + Facial combined model                |
| `6_ei_analysis.ipynb`                    | EI-based performance comparison            |

---

## 📦 Installation

```bash
git clone https://github.com/your-org/etri-emotion.git
cd etri-emotion
conda env create -f environment.yml
conda activate etri-emotion
jupyter lab
