# Deep Learning on MNIST

## Project Overview
This repository collects a series of deep learning experiments on the MNIST dataset, covering both discriminative and generative models.

The project includes:
- supervised learning with MLPs and CNNs
- analysis of the double descent phenomenon
- transfer learning on rotated digit classification
- dimensionality reduction with autoencoders
- generative modeling with a GAN

The goal is to explore how different neural architectures and training setups affect optimization, generalization, representation learning, and sample generation.

---

## Contents

### 1. Supervised Learning
Two neural network architectures were compared for handwritten digit classification:
- Multi-Layer Perceptron (MLP)
- Convolutional Neural Network (CNN)

The CNN outperformed the MLP on the MNIST test set, reaching about 98.6% accuracy, while the MLP achieved about 97.8%.

### 2. Double Descent
A set of experiments was designed to study the double descent phenomenon by varying model width on a fixed subset of MNIST.

Two training setups were compared:
- stochastic gradient descent with cross-entropy loss
- full-batch training with mean squared error

The results show that generalization behavior depends not only on model capacity, but also on the optimization setup.

### 3. Transfer Learning
Transfer learning was studied using a CNN pre-trained on MNIST and adapted to rotated-digit classification tasks.

Two scenarios were tested:
- random rotations up to 30 degrees
- fixed rotations of 90 degrees

With limited training data, transfer learning outperformed training from scratch:
- 30° rotation: transfer learning reached about **95.69% accuracy**
- 90° rotation: transfer learning reached about **90.38% accuracy**

### 4. Autoencoders
Two autoencoder architectures were trained to learn a 2D latent representation of MNIST digits.

The experiments show that increasing encoder depth improves the structure and separability of the learned latent space.

### 5. Generative Models
A DCGAN-style generative model was trained on MNIST to generate handwritten digits.

The generated samples became progressively more structured during training, although the adversarial optimization remained unstable and sample quality was uneven across epochs.

---

## Technologies Used
- Python
- PyTorch
- NumPy
- Matplotlib
- Jupyter Notebook



## Repository Structure

```
deep-learning-mnist/
│
├── notebooks/
│   ├── task1_mlp_vs_cnn.ipynb
│   ├── task2_double_descent.ipynb
│   ├── task3_transfer_learning.ipynb
│   ├── task4.ipynb
│   └── task5.ipynb
│
├── report.pdf
└── README.md
```


## Key Takeaways
This project explores several core topics in deep learning:
- image classification
- optimization and generalization
- transfer learning under limited data
- representation learning
- generative modeling

It provides a compact overview of different deep learning paradigms through a common benchmark dataset.

---

## Author
Project developed as part of university coursework in Neural Networks and Deep Learning.
