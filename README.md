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

![CondFoodGen framework](figures/condfoodgen.png)


**Bidirectional Adaptive Gating (BAG)** enables dynamic cross‑stream interaction.  
<p align="center">
  <img src="figures/BAG.png" alt="BAG module" width="350">
</p>

**Wavelet‑Guided Hierarchical Attention (WGHA)** refines multi‑frequency features.  
![WGHA module](figures/WGHA.png)

## 📊 Quantitative Results

<div align="center">

### Comparison with food‑specific generation methods

<img src="figures/Quantitative%20result1.png">

### Comparison with conditional control methods

<img src="figures/Quantitative%20result2.png">

</div>

## 🚀 Getting Started

### Environment Setup

We recommend using a virtual environment (Python 3.8+).

#### PyTorch 1.13 (CUDA 11.7)
```bash
python3 -m venv .pt13
source .pt13/bin/activate          # Linux/macOS
# .pt13\Scripts\activate           # Windows
pip install -r requirements/pt13.txt

## 🧪 Training

We provide a single training script `main.py` with a three‑phase progressive strategy.

### Prerequisites

- Download and prepare the dataset (e.g., VIREO Food‑172, Recipe1M, Food2K).  
- Place the dataset root path in the config file `configs/training/sd/sd15_encD_canny_53m.yaml` (modify `data.params.train.root` and `data.params.validation.root`).
- (Optional) Download a pretrained Stable Diffusion 1.5 checkpoint and set its path in the config.

### Training Command

```bash
python main.py -t --base configs/training/sd/sd15_encD_canny_53m.yaml --logdir ./logs --name your_experiment_name
