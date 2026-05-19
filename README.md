# CIFAR-10 Image Classification using Convolutional Neural Networks (CNN)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)
![Dataset](https://img.shields.io/badge/Dataset-CIFAR10-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

# Project Overview

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** for multi-class image classification on the CIFAR-10 dataset.

The objective of this project is to build and train a deep learning model capable of classifying RGB images into 10 different categories using convolutional operations, pooling layers, activation functions, and fully connected neural networks.

This project demonstrates the complete deep learning workflow including:

- Data preprocessing
- Image transformations
- Dataset handling
- DataLoader implementation
- CNN model creation
- Model training
- Model evaluation
- Accuracy calculation

---

# Dataset Information

This project uses the CIFAR-10 dataset from torchvision.

The dataset contains:

- 60,000 RGB images
- Image size: 32 × 32
- 10 image classes
- 50,000 training images
- 10,000 testing images

## Classes

| Label | Class |
|------|------|
| 0 | Airplane |
| 1 | Automobile |
| 2 | Bird |
| 3 | Cat |
| 4 | Deer |
| 5 | Dog |
| 6 | Frog |
| 7 | Horse |
| 8 | Ship |
| 9 | Truck |

---

# Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas

---

# Deep Learning Concepts Used

This project includes the implementation of:

- Convolutional Neural Networks (CNN)
- Image Preprocessing
- Tensor Operations
- Forward Propagation
- Backpropagation
- Gradient Descent
- Loss Functions
- Optimizers
- Model Evaluation

---

# Project Workflow

## 1. Data Preprocessing

Image transformations were applied using torchvision transforms.

### Transformations Used

- Convert images to tensors
- Normalize pixel values

```python
transform = transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize((0.5,), (0.5,))
])
```

---

## 2. Dataset Loading

The CIFAR-10 dataset was loaded using torchvision datasets.

```python
train_dataset = datasets.CIFAR10(
    root='./data',
    train=True,
    download=True,
    transform=transform
)
```

---

## 3. DataLoader Implementation

PyTorch DataLoader was used for batching and shuffling the dataset during training.

```python
train_loader = DataLoader(
    train_dataset,
    batch_size=64,
    shuffle=True
)
```

---

## 4. CNN Architecture

The CNN model consists of:

- Convolutional Layers
- ReLU Activation Functions
- Max Pooling Layers
- Fully Connected Layers

### Layers Used

```python
nn.Conv2d()
nn.ReLU()
nn.MaxPool2d()
nn.Linear()
```

---

## 5. Model Training

The model was trained using:

- CrossEntropyLoss
- Adam Optimizer
- Forward Propagation
- Backpropagation

### Training Process

1. Forward Pass
2. Loss Calculation
3. Gradient Calculation
4. Weight Update
5. Repeat for multiple epochs

---

## 6. Model Evaluation

The trained model was evaluated on the testing dataset.

### Evaluation Metrics

- Accuracy Score

```python
with torch.no_grad():
    outputs = model(images)
```

---

# Model Performance

| Metric | Value |
|------|------|
| Training Dataset | CIFAR-10 |
| Number of Classes | 10 |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |
| Framework | PyTorch |
| Test Accuracy | 75.69% |

---

![image alt](https://github.com/Anurag1466/CNN-Image-Classification-using-CIFAR-10/blob/6e199e11ccb6cb98b8e846a147c87aec51aa02cb/Screenshot%202026-05-19%20180221.png)

# Project Structure

```text
cifar10-cnn-project/
│
├── models/
│   └── cnn_model.pth
│
├── src/
│   ├── model.py
│   ├── train.py
│   ├── evaluate.py
│   └── predict.py
│
├── outputs/
│   ├── accuracy_graph.png
│   └── sample_predictions.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Installation

## Clone the Repository

```bash
https://github.com/Anurag1466/CNN-Image-Classification-using-CIFAR-10.git
```


## Install Required Libraries

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Train the Model

```bash
python train.py
```

## Evaluate the Model

```bash
python evaluate.py
```

---

# Sample Output

Example Prediction:

```text
Predicted Class: Cat
Actual Class: Cat
```

---

# Future Improvements

- Improve model accuracy
- Add Dropout layers
- Implement Batch Normalization
- Train deeper CNN architectures
- Deploy model using Streamlit

---

# Learning Outcomes

Through this project, the following concepts were learned and implemented:

- CNN Architecture Design
- PyTorch Deep Learning Workflow
- Image Classification
- Dataset Handling
- Model Training and Evaluation
- Deep Learning Fundamentals

---

# License

This project is created for educational and learning purposes.

---
