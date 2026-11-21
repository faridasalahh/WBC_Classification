# White Blood Cell Classification

A computer-vision project for classifying white blood cell images using deep learning and image-feature techniques.

## Project overview

This project explores an image-classification workflow for white blood cell (WBC) images. The implementation uses **PyTorch** and an **EfficientNet-B3** backbone, alongside SIFT-based image features as part of the feature-extraction experiments.

The repository is intended for educational and research use. It is not a clinical diagnostic tool.

## Technical approach

- **Image input:** images are resized to 224 × 224 pixels.
- **Deep learning:** EfficientNet-B3 implemented with PyTorch.
- **Image features:** SIFT (Scale-Invariant Feature Transform) experiments.
- **Training strategy:** class-aware sampling with `WeightedRandomSampler` and class-weighted cross-entropy to help address class imbalance.
- **Evaluation:** report per-class precision, recall, F1-score, confusion matrix, and overall metrics when running the experiments.

## Technology

- Python
- PyTorch
- torchvision
- OpenCV (for SIFT / image processing)
- NumPy and Pandas
- Matplotlib

## Getting started

Clone the repository:

```bash
git clone https://github.com/faridasalahh/WBC_Classification.git
cd WBC_Classification
```

Create and activate a virtual environment (macOS / Linux):

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies used by the project:

```bash
python -m pip install --upgrade pip
pip install torch torchvision opencv-python numpy pandas matplotlib scikit-learn
```

> For GPU acceleration, install the PyTorch build that matches your operating system and hardware. On Apple Silicon, use the standard PyTorch installation and check MPS availability in your environment.

Open the relevant notebook(s) in the repository to explore preprocessing, training, and evaluation.

## Reproducibility and reporting

For a reproducible experiment, document the dataset source and license, class names and counts, train/validation/test split, random seed, optimizer, learning rate, number of epochs, and model checkpoint selection.

No benchmark scores are stated here because verified evaluation results were not available in the repository documentation at the time this README was prepared. Add measured results and a confusion matrix once confirmed.

## Responsible use

WBC image classification is a medical-imaging research task. Model predictions can be wrong and must not be used to make clinical decisions.

## Author

Farida Sheref Salah

## License

No license is currently specified. All rights remain with the respective rights holders unless a license is added.
