# CondFoodGen
# CondFoodGen

**A Conditional Two‑Stream Network for Controllable Food Image Generation**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-1.13+-red.svg)](https://pytorch.org/)

## 📝 Overview

CondFoodGen is a diffusion‑based framework for generating realistic and semantically consistent food images from **recipe texts** and **structural conditions** (edge/depth maps). It introduces two key innovations:

- **Bidirectional Adaptive Gating (BAG)** – enables dynamic, context‑aware interaction between the control stream and the generation stream.
- **Wavelet‑Guided Hierarchical Attention (WGHA)** – refines multi‑frequency features to preserve fine‑grained textures and global structures.

## 🏗️ Framework

![Framework](figures/framework.png)

## 📊 Results

Comparison with state‑of‑the‑art methods on VIREO Food‑172, Recipe1M, and Food2K:

![Quantitative results](figures/results.png)

### Sample Generations

![Examples](figures/examples.png)

## 🚀 Getting Started

### Environment Setup

We recommend using a virtual environment (Python 3.8+).

#### PyTorch 1.13 (CUDA 11.7)
```bash
python3 -m venv .pt13
source .pt13/bin/activate          # Linux/macOS
# .pt13\Scripts\activate           # Windows
pip install -r requirements/pt13.txt
