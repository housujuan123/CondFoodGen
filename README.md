# CondFoodGen
A Conditional Two-Stream Network for Controllable Food Image Generation
# CondFoodGen

**A Conditional Two-Stream Network for Controllable Food Image Generation**

This repository contains the official implementation of **CondFoodGen**, a diffusion-based framework that generates high-fidelity and semantically consistent food images conditioned on recipe texts and structural guidance (edge/depth maps).

## 📝 Paper
[Link to your paper – add URL when available]

## ✨ Key Features
- 🔀 **Two-stream architecture** – separate control stream and generation stream.
- 🔄 **Bidirectional Adaptive Gating (BAG)** – dynamic cross-stream interaction.
- 🌊 **Wavelet-Guided Hierarchical Attention (WGHA)** – multi-frequency feature refinement for texture and structure.
- 📊 **State-of-the-art performance** on VIREO Food-172, Recipe1M, and Food2K.

## 🚀 Getting Started

### Requirements
- Python 3.8+
- PyTorch 1.10+
- etc.

### Installation
```bash
git clone https://github.com/housujuan123/CondFoodGen.git
cd CondFoodGen
pip install -r requirements.txt
