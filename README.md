# OWASP Attack Classifier

A deep learning-based sequence classification system that uses PyTorch and custom neural networks to detect malicious web traffic anomalies and OWASP-based attacks.

---

# Overview

This project demonstrates how deep learning techniques can be applied to cybersecurity and web application protection.

The system treats raw HTTP requests as sequential text data, preprocesses them using custom tokenization and vocabulary encoding, and classifies requests as either:

- Normal Traffic
- Malicious Attack

The project compares multiple deep learning architectures including:

- MLP
- MLP + Batch Normalization
- LSTM
- GRU

Among all tested models, the GRU model achieved the best performance.

---

# Features

- HTTP request preprocessing
- Custom text cleaning using Regex
- Tokenization and vocabulary generation
- Sequence padding
- Deep learning-based attack classification
- Multiple neural network comparisons
- Attack probability prediction
- Training loss visualization
- Interactive request testing

---

# Attack Types Tested

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Path Traversal
- OWASP-based malicious payloads

---

# Tech Stack

- Python
- PyTorch
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

# Project Structure

```text
owasp-attack-classifier/
│
├── dataset/
│   ├── normalTrafficTraining.txt
│   └── anomalousTrafficTest.txt
│
├── owasp-attack-classifier.ipynb
├── requirements.txt
└── README.md
```

---

# Dataset

The dataset contains:

- Normal HTTP traffic requests
- Malicious web attack requests

Example normal request:

```http
GET /products.php?id=10 HTTP/1.1
```

Example malicious request:

```http
GET /login.php?id=' OR 1=1 --
```

---

# Models Implemented

## 1. MLP (Multi-Layer Perceptron)

A fully connected neural network used as the baseline model.

---

## 2. MLP + Batch Normalization

Enhanced MLP architecture with Batch Normalization for improved training stability.

---

## 3. LSTM (Long Short-Term Memory)

A recurrent neural network designed for sequential learning.

---

## 4. GRU (Gated Recurrent Unit)

An optimized recurrent neural network architecture that achieved the best performance in this project.

---

# Training Results

| Model | Accuracy |
|------|------|
| MLP | 56.77% |
| MLP + BatchNorm | 59.47% |
| LSTM | 49.82% |
| GRU | 70.38% |

✅ GRU achieved the highest accuracy among all tested models.

---

# Model Comparison

The project visualizes training loss comparison between all implemented models using Matplotlib.

Example compared models:

- MLP
- MLP + BN
- LSTM
- GRU

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/owasp-attack-classifier.git
```

```bash
cd owasp-attack-classifier
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Run the Project

Open Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```text
owasp-attack-classifier.ipynb
```

---

# Example Inputs

## Normal Request

```http
GET /products.php?id=10 HTTP/1.1
```

---

## SQL Injection

```http
GET /login.php?id=' OR 1=1 --
```

---

## Cross-Site Scripting (XSS)

```http
GET /search.php?q=<script>alert(1)</script>
```

---

## Path Traversal

```http
GET ../../etc/passwd
```

---

# Example Output

```text
Request:
GET /login.php?id=' OR 1=1 --

Attack Probability: 0.81

⚠️ MALICIOUS OWASP ATTACK DETECTED
```

---

# Evaluation Metrics

The project evaluates models using:

- Accuracy Score
- Training Loss
- Attack Probability
- Comparative Visualization

---

# Requirements

Example `requirements.txt`

```txt
torch
scikit-learn
matplotlib
numpy
jupyter
```

---

# Future Improvements

- Add larger cybersecurity datasets
- Improve model accuracy
- Implement Transformer-based models (BERT)
- Build a Flask/FastAPI web application
- Deploy as a real-time API service
- Add live traffic monitoring
- Integrate packet analysis tools

---

# License

MIT License

---

# Author

Padmesh B

---

# GitHub Repository

```text
https://github.com/YOUR_USERNAME/owasp-attack-classifier
```
