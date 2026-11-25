# CIFAR-100: Custom CNN vs. Transfer Learning

Deep Learning coursework (BTH) in TensorFlow/Keras.

## Contents
- **Part 1 – Gradient descent from scratch:** minimising f(x, y) = (x-3)² + (y+2)² with hand-derived gradients, loss curve and optimisation trajectory plots (NumPy, Matplotlib).
- **Part 2 – Image classification on CIFAR-100:** a custom 6-layer CNN (with Batch Normalization and Dropout) compared with four ImageNet pre-trained backbones (frozen, new classification head).

## Results (CIFAR-100 test accuracy)
| Model | Accuracy |
|---|---|
| EfficientNet-B0 | 0.543 |
| DenseNet-121 | 0.514 |
| ResNet-50 | 0.486 |
| VGG-19 | 0.461 |
| Custom CNN | 0.340 |

Pre-trained models win because their features come from ~1.2M ImageNet images; fine-tuning the backbones would likely improve them further.

## Files
- `assignment_1.ipynb` – code and outputs
- `Assignment1_Report.pdf` – full report

## Running
Download CIFAR-100 (python version) from https://www.cs.toronto.edu/~kriz/cifar.html and extract it as `cifar-100-python/` next to the notebook. The dataset is not included in this repository.

```bash
pip install tensorflow numpy pandas matplotlib
jupyter notebook assignment_1.ipynb
```
