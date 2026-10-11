# FashionMNIST_Project

Image classification on Fashion-MNIST dataset using Convolutional Neural Networks (CNN) in PyTorch.

## Overview
This project compares a baseline CNN vs an improved CNN with data augmentation and regularization.

## Dataset
- **Fashion-MNIST**: 70,000 grayscale images (28x28) of 10 fashion categories
- 60,000 training / 10,000 test
- Classes: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot

## Results

| Metric | Baseline CNN | Improved CNN | Change |
| :--- | :--- | :--- | :--- |
| Accuracy | 0.9117 | 0.9363 | +0.0246 |
| Precision | 0.9138 | 0.9364 | +0.0226 |
| Recall | 0.9117 | 0.9363 | +0.0246 |
| F1-Score | 0.9123 | 0.9363 | +0.0240 |

**Improvement: +2.46% accuracy**

## Key Improvements
- Data Augmentation (Random Horizontal Flip, Rotation)
- Batch Normalization
- Dropout Regularization
- Adam optimizer with learning rate scheduling

## Error Analysis
Confusion matrix analysis shows the most common confusions are:
- Shirt vs T-shirt/top
- Pullover vs Coat
- Sandal vs Sneaker

The improved model significantly reduces these off-diagonal errors.

## How to Run
```bash
pip install torch torchvision matplotlib scikit-learn seaborn
jupyter notebook FashionMNIST_Project.ipynb
