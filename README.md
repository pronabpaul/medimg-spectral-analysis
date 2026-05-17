# Modality-Aware Frequency and Texture Characterisation of Medical Imaging Datasets

**Author:** Pronab Kumar Paul

## Overview

This repository contains a reproducible Jupyter notebook for analysing modality‑specific frequency and texture statistics in medical imaging datasets using classical frequency and texture descriptors.

The study compares:

* **OrganSMNIST** (CT‑derived anatomical slices)
* **PathMNIST** (histopathology image patches)

from the MedMNIST v3 benchmark using:

* Fourier spectral analysis (FFT power‑law estimation)
* Multi‑scale Local Binary Patterns (LBP)
* Gray‑Level Co‑occurrence Matrix (GLCM) statistics

The objective is to quantify differences in frequency structure, texture organisation, and colour‑dependent spatial statistics across modalities, and to investigate their implications for modality‑aware representation learning in medical imaging.

The analysis reveals measurable modality‑dependent differences in spectral decay behaviour, local texture structure, and spatial correlation statistics between CT‑derived anatomical imagery and histopathology patches.



## Features

The notebook includes:

* FFT‑based radial power spectrum estimation
* Spectral slope (α) fitting using robust RANSAC regression
* Multi‑scale uniform LBP analysis
* Multi‑distance and multi‑angle GLCM extraction
* RGB / HSV / LAB texture analysis
* Statistical hypothesis testing
  * Mann‑Whitney U
  * Kruskal‑Wallis
  * Cliff’s delta
* Gaussian noise robustness analysis
* t‑SNE visualisation
* Exploratory Random Forest feature importance analysis



## Datasets

The experiments use the following MedMNIST datasets:

| Dataset     | Modality                  | Classes | Colour    |
| ----------- | ------------------------- | ------- | --------- |
| OrganSMNIST | CT‑like anatomical slices | 11      | Grayscale |
| PathMNIST   | Histopathology patches    | 9       | RGB       |

All datasets are automatically downloaded via the `medmnist` Python package.



## Run in Google Colab

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `spectral_analysis.ipynb`
3. Run all cells (`Runtime → Run all`)

The notebook automatically installs required dependencies.



## Reproducibility

* Random seed: `42`
* MedMNIST version: `v3`
* Python version: `3.12` (Colab default)
* Fully self‑contained notebook pipeline



## Repository Structure

```text
.
├── spectral_analysis.ipynb
├── README.md
├── LICENSE
├── requirements.txt
└── .gitignore
