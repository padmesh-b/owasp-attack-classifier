# OWASP Attack Classifier

This repository contains a PyTorch-based Deep Learning pipeline designed to detect malicious web traffic (such as SQL Injection, Cross-Site Scripting, and Path Traversal) by analyzing HTTP requests.

## 🧠 Overview
The project treats HTTP logs as sequential text data. It processes raw web requests, builds a custom vocabulary, and compares several neural network architectures to classify sequences as either `Normal` or `Attack`. 

## 📁 Repository Structure
* `1.ipynb`: The main Jupyter Notebook containing data preprocessing, model definitions, training loops, and evaluation.
* `dataset/`: Contains the raw text logs used for training and testing.

## 🛠️ Tech Stack
* **Language:** Python
* **Deep Learning:** PyTorch (`torch.nn`, `torch.optim`)
* **Data Processing:** Scikit-learn, Collections, Regex
* **Visualization:** Matplotlib

## 📊 Models & Architecture
The project evaluates four different models to determine the best architecture for sequence-based anomaly detection:
1. **MLP (Multi-Layer Perceptron):** Standard feedforward network with Embedding and Linear layers.
2. **MLP + Batch Normalization:** Enhanced MLP utilizing `BatchNorm1d` for training stability.
3. **LSTM (Long Short-Term Memory):** Recurrent network for capturing sequence dependencies.
4. **GRU (Gated Recurrent Unit):** Streamlined recurrent model.

## 📈 Results & Evaluation
Based on the validation testing, the models achieved the following accuracy scores:
* **GRU:** ~70.3% (Best Performing)
* **MLP + BatchNorm:** ~59.4%
* **MLP:** ~56.7%
* **LSTM:** ~49.8%

The GRU model demonstrated the fastest convergence and highest accuracy for identifying OWASP-style attacks within the dataset.

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies: `pip install torch scikit-learn matplotlib`
3. Ensure your dataset files are inside the `dataset/` directory.
4. Run `1.ipynb` to train the models and test custom HTTP requests.
