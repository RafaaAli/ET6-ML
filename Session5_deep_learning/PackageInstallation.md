# Pre-Class Setup: Install PyTorch or TensorFlow & Check Your System

Welcome! Before our upcoming session, please follow the instructions below to make sure you're ready to work with deep learning tools like **PyTorch** or **TensorFlow**.

---

## CPU vs GPU: What’s the Difference?

| Feature        | CPU                           | GPU                              |
|----------------|-------------------------------|----------------------------------|
| General use    | Everyday computing tasks       | Graphics, games, machine learning |
| Cores          | Few (2–16), powerful           | Thousands of small cores         |
| ML performance | Slower                         | Much faster for training deep models |

A **GPU (Graphics Processing Unit)** is highly efficient at performing many calculations in parallel. It speeds up model training significantly compared to a **CPU (Central Processing Unit)**. If you don’t have a dedicated GPU, don’t worry—you can still do everything with a CPU (just slower).

---

## How to Know If You Have a GPU

### In PyTorch:
```python
import torch

if torch.cuda.is_available():
    print("GPU is available:", torch.cuda.get_device_name(0))
else:
    print("No GPU found. You're using CPU.")
```
### In TensorFlow:
```python
import tensorflow as tf

gpus = tf.config.list_physical_devices('GPU')
if gpus:
    print("GPU is available:", gpus)
else:
    print("No GPU found. You're using CPU.")
```

### Google Colab Users
If you're using Google Colab, you can enable GPU for free:

- Go to Runtime → Change runtime type

- Select GPU from the dropdown

- Then run the code above to check your GPU

No need to install anything manually—Colab comes pre-installed with both PyTorch and TensorFlow (with GPU support).

## Installation Instructions
You only need to install one of the following: PyTorch or TensorFlow.

### Option 1: PyTorch (Recommended for flexibility)
For GPU-enabled systems (CUDA):
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

For CPU-only systems:
```bash

pip install torch torchvision torchaudio
```

Test the installation:

```python
import torch
print("GPU Available:", torch.cuda.is_available())
```

### Option 2: TensorFlow
Install (CPU or GPU version auto-detected):
``` bash
pip install tensorflow
```

Test the installation:

```python
import tensorflow as tf
print("Num GPUs Available:", len(tf.config.list_physical_devices('GPU')))
```
### Need Help?
If you're unsure whether to install the CPU or GPU version, or run into errors during setup, feel free to ask during the session or reach out ahead of time.

Let’s get ready to build and train some models

