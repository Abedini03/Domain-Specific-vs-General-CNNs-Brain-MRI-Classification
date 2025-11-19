# Domain-Specific vs General CNNs for Brain MRI Classification

[![arXiv](https://img.shields.io/badge/arXiv-2104.00298-b31b1b.svg)](https)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)](https://www.tensorflow.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

![image](11.png)

**Official repository for the paper:**  
**"General vs Domain-Specific CNNs: Understanding Pretraining Effects on Brain MRI Tumor Classification"**

*Helia Abedini, Saba Rahimi, and Reza Vaziri*  

## Overview

This repository contains the complete implementation for our research paper comparing domain-specific versus general-purpose pretrained CNNs for brain tumor classification from MRI scans. The study systematically evaluates three pretrained models under identical small-data conditions:

- **RadImageNet DenseNet121** (domain-specific medical pretraining) (https://github.com/BMEII-AI/RadImageNet)
- **EfficientNetV2S** (general-purpose ImageNet pretraining) (https://github.com/da2so/efficientnetv2)
- **ConvNeXt-Tiny** (modern general-purpose ImageNet pretraining) (https://github.com/facebookresearch/ConvNeXt)

## Key Findings

| Model                     | Pretraining Type         | Accuracy | AUC-ROC |
|---------------------------|--------------------------|----------|---------|
| ConvNeXt-Tiny             | General (ImageNet)       | **93%**  | **98.5%** |
| EfficientNetV2S           | General (ImageNet)       | 85%      | 96%     |
| RadImageNet DenseNet121   | Medical (RadImageNet)    | 68%      | 88%     |

**Main Conclusion:** Modern general-purpose CNN architectures pretrained on large-scale natural image datasets outperform domain-specific medical pretraining when limited annotated medical data is available.

## Quick Start

### Prerequisites

```bash
# Clone this repository
git clone https://github.com/your-username/domain-specific-vs-general-cnns-brain-mri.git
cd domain-specific-vs-general-cnns-brain-mri

# Install dependencies
pip install -r requirements.txt
