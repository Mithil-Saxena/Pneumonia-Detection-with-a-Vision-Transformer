# Vision Transformer Image Classification

A computer vision project exploring Hugging Face Vision Transformer (ViT) fine-tuning, CLAHE image preprocessing, raw/CLAHE fusion, and test-time augmentation (TTA).

## Overview

This project compares eight model configurations to evaluate how preprocessing, fine-tuning strategies, and inference-time augmentation affect image classification performance.

## Experiments

The experiments compare:

- Reference ViT using raw images
- Reference ViT using CLAHE-preprocessed images
- Fine-tuned ViT with class weighting
- Fine-tuned ViT without class weighting
- Fine-tuned ViT with CLAHE
- Reference ViT with test-time augmentation
- Reference ViT with raw/CLAHE fusion
- Raw/CLAHE fusion combined with test-time augmentation

## Results

The best-performing configuration in the recorded experiments was the reference ViT with raw/CLAHE fusion.

| Metric | Result |
|---|---:|
| Accuracy | 97.92% |
| Precision | 97.72% |
| Recall | 98.97% |
| F1 Score | 98.34% |
| ROC-AUC | 99.63% |

These metrics are based on the recorded evaluation results. Performance on other datasets may differ.

Detailed experiment results are available in [`results/vit_results.csv`](results/vit_results.csv).

## Repository Structure

```text
vit-image-classification/
├── notebooks/
│   └── vit_finetuning.ipynb
├── results/
│   └── vit_results.csv
├── .gitignore
├── requirements.txt
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/vit-image-classification.git
cd vit-image-classification
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows**
```bash
.venv\Scripts\activate
```

**Linux/macOS**
```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook notebooks/vit_finetuning.ipynb
```

Dataset paths, model access requirements, and compute requirements must be configured according to the notebook.

## Dataset

The dataset is not included in this repository. Use the original dataset source and follow its license, access conditions, and usage restrictions.

## Limitations

- Results depend on the dataset, preprocessing, and evaluation setup.
- The reported metrics do not establish generalization to external datasets.
- Additional validation is necessary before any real-world or clinical application.

## Reproducibility

For reproducible comparisons, document the model checkpoint, dataset split, random seeds, preprocessing settings, dependency versions, and evaluation procedure.

## License

A license has not yet been selected. Add one after confirming that you have the right to distribute the code and related materials.
