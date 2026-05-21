# OWASP Attack Classifier

A deep learning-based sequence classification system that uses PyTorch and custom neural networks to detect malicious web traffic anomalies.

---

## Overview

This project demonstrates how deep learning techniques can be used to build a robust web application firewall (WAF) classifier. 
By treating HTTP logs as sequential text data, the system analyzes raw web requests, builds a custom vocabulary, and evaluates the sequences to classify them as either `Normal` or `Attack`.

---

## Features

* Accepts raw, free-text HTTP request input
* Cleans and tokenizes text using custom Regex and vocabulary mapping
* Trains and compares multiple neural network architectures (MLP, LSTM, GRU)
* Computes a probability score for malicious intent (0 to 1)
* Evaluates model performance and visualizes training loss

---

## Tech Stack

* Python
* PyTorch
* Scikit-learn
* Matplotlib
* NumPy

---

## Project Structure

```text
owasp-attack-classifier/
├── dataset/
│   ├── normalTrafficTraining.txt
│   └── anomalousTrafficTest.txt
├── owasp-attack-classifier.ipynb
├── requirements.txt
└── README.md
