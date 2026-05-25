# Garbage Image Classification

A binary image classification project: clean vs dirty waste. Compares three
approaches on a small image dataset — a neural network coded from scratch
in NumPy, a CNN in PyTorch, and a CNN in TensorFlow/Keras.

**Tech stack:** NumPy · PyTorch · TensorFlow · PIL · scikit-learn

## Approach

- **Dataset:** ~140 images (clean + dirty waste), split 80/20 train/test
- **EDA:** image sizes, RGB & grayscale histograms, corrupted-file check
- **Preprocessing:** resize to 32×32, grayscale conversion, normalization
- **Models compared:**
  - Manual neuron in NumPy (logistic regression with L1/L2 regularization,
    custom forward/backward pass)
  - CNN with PyTorch
  - CNN with TensorFlow/Keras
- **Goal:** build intuition by re-implementing what high-level frameworks
  abstract away, then benchmark against them

## Installation

```bash
git clone https://github.com/MEMAUDATA/garbage-classification.git
cd garbage-classification

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage

```bash
jupyter notebook garbage.ipynb
```

Run all cells to reproduce the EDA, train the three models, and compare
their accuracy on the test set.

## Limitations

- Very small dataset (~140 images) — results are exploratory, not production-ready
- No data augmentation applied
- Models may benefit from transfer learning (e.g. ResNet pretrained on ImageNet)

## License

This project is licensed under the **MIT License** —
see the [LICENSE](LICENSE) file for details.

## Author

**Nicolas Vannson** — Hearing Data Scientist
[memaudata.github.io](https://memaudata.github.io)