# ECSC: Energy-Calibrated Semantic Communication

**Ziyu Wang¹, Yiming Du¹, Rui Ning¹, Daniel Takabi², and Lusi Li¹**

¹ Department of Computer Science, Old Dominion University, Norfolk, VA, USA  
² School of Cybersecurity, Old Dominion University, Norfolk, VA, USA

📄 **Paper Available on [IEEE Xplore](https://ieeexplore.ieee.org/document/11310481)**

🔗 **[Paper](https://ieeexplore.ieee.org/document/11310481)** | **[Code](https://github.com/sunway677/ECSC)**

---

## 📖 Overview

**ECSC (Energy-Calibrated Semantic Communication)** is an end-to-end semantic communication framework designed to preserve semantic information and improve reconstruction robustness under noisy wireless channels.

To address these limitations, ECSC integrates **multi-scale hierarchical feature learning**, **energy-based semantic calibration**, and **topology-preserving regularization** into a unified communication framework.

Specifically, ECSC employs a **multi-scale U-Net autoencoder** with ResNet backbones to learn hierarchical representations, together with lightweight compression and decompression modules for efficient transmission. A trainable **energy-based model (EBM)**, guided by a pre-trained CLIP vision encoder, promotes semantic alignment between original and reconstructed images.

To further improve semantic and structural consistency, ECSC incorporates:

- **Energy-weighted image reconstruction** to encourage semantically faithful reconstruction.
- **Multi-scale feature reconstruction** to preserve hierarchical feature representations.
- **Sparsity regularization** to encourage compact feature representations.
- **K-nearest neighbor (KNN) topology regularization** to preserve relationships among latent features without requiring class labels.

Experiments on **CIFAR-10 over additive white Gaussian noise (AWGN) channels** demonstrate improved semantic fidelity, reconstruction quality, and robustness, particularly under low signal-to-noise ratio (SNR) conditions.

This repository provides the **official PyTorch implementation** of ECSC.

## 🏗️ System Architecture

![ECSC Architecture](./ECSC.png)

*Overview of the proposed ECSC framework, integrating hierarchical feature learning, semantic calibration, and topology-preserving regularization.*

## ⚙️ Requirements

The implementation is based on Python and PyTorch.

**Core Dependencies**

- Python 3.x
- PyTorch
- Transformers (for CLIP)
- NumPy
- Matplotlib
- scikit-image
- tqdm

Install the required packages using:

```bash
pip install torch transformers numpy matplotlib scikit-image tqdm
```

For reproducibility, we recommend using a dedicated Python environment and installing package versions compatible with your CUDA and PyTorch configurations.

## 📚 Citation

If you find this repository useful in your research, please cite our paper:

**Ziyu Wang, Yiming Du, Rui Ning, Daniel Takabi, and Lusi Li.**  
"[ECSC: Energy-Calibrated Semantic Communication](https://ieeexplore.ieee.org/document/11310481)."  
*Proceedings of the IEEE Military Communications Conference (MILCOM)*, pp. 1359–1364, 2025.

```bibtex
@inproceedings{wang2025ecsc,
  title={ECSC: Energy-Calibrated Semantic Communication},
  author={Wang, Ziyu and Du, Yiming and Ning, Rui and Takabi, Daniel and Li, Lusi},
  booktitle={MILCOM 2025 - 2025 IEEE Military Communications Conference (MILCOM)},
  pages={1359--1364},
  year={2025},
  organization={IEEE}
}
```
## 📬 Contact

For questions regarding the implementation, experimental results, or research collaboration, please open an issue in this repository or contact the authors.
