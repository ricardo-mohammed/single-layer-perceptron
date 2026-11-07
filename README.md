# Single Layer Perceptron Workshop - Group 3

## Project Overview
This repository contains our implementation of the Single Layer Perceptron (SLP) workshop. It demonstrates fundamental concepts of artificial neural networks, perceptron learning algorithms, and binary classification tasks, including the Canada's Wonderland case study.

## Team Members - Group 3

| Name | Student ID |
|------|------------|
| Juan Camilo Chirivi  | 9115141 |
| Zeynep Ozdemir       | 9045142 |
| Senay Teweldebrhan   | 9120588 |
| Ricardo Mohammed     | 7500382 |


## Prerequisites
- Python 3.8 or higher
- pip (Python package installer)
- Virtual environment tool (venv)

## Installation Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

## 🛠️ Installation Instructions

### Prerequisites

This project requires **Python 3.12** (3.11 or 3.13 also work). TensorFlow 2.20.0 does **not** support Python 3.14, so the setup below verifies your Python version before creating the environment.

### 1. Verify Your Python Version

**Windows (Bash in VSCode):**

    py -3.12 --version

If this fails, install Python 3.12 first:

    winget install Python.Python.3.12

Then restart your terminal and run the version check again.

**macOS/Linux:**

    python3.12 --version

If this fails, install Python 3.12 (e.g., `brew install python@3.12` on macOS, or `sudo apt install python3.12` on Ubuntu), then run the version check again.

You should see `Python 3.12.x` printed. **Do not proceed if the version shown is 3.14 or higher.**

### 2. Create and Activate Virtual Environment

**Windows:**

    py -3.12 -m venv .venv
    source .venv/Scripts/activate

**macOS/Linux:**

    python3.12 -m venv .venv
    source .venv/bin/activate

**Confirm the virtual environment is using Python 3.12:**

    python --version

This must print `Python 3.12.x`. If it shows a different version, delete the `.venv` folder and repeat this step.

### 3. Install Dependencies

    python -m pip install --upgrade pip
    pip install -r requirements.txt

### 4. Verify the TensorFlow Installation

    python -c "import tensorflow as tf; print('TensorFlow', tf.__version__)"

This should print the TensorFlow version without any errors.

## Project Structure
```text
SingleLayerPerceptron_Workshop/
├── SingleLayerPerceptrons_Workshop.ipynb    # Original workshop notebook
├── SingleLayerPerceptrons_Workshop-solution.ipynb  # Completed solution notebook
├── requirements.txt                          # Python dependencies
├── README.md                                 # This file
└── .gitignore                               # Git ignore file
```

## Usage

### Running the Notebook
After activating your virtual environment, launch Jupyter Notebook and open the solution file:
```bash
jupyter notebook SingleLayerPerceptrons_Workshop-solution.ipynb
```

### Key Topics Covered
1. **Perceptron Fundamentals:** Understanding the basic unit of neural networks.
2. **Activation Functions:** Step function implementation.
3. **Weight Updates:** Learning rule implementation and Gradient Descent.
4. **Logic Gates:** AND, OR, NOT gate implementations.
5. **Linear Separability:** Understanding perceptron limitations (XOR problem).
6. **Real-world Application:** Canada's Wonderland Case Study.

## 🧠 Key Concepts: The Single-Neuron ANN

Our prostate cancer prediction example, while simple, demonstrates the fundamental mechanics of a single artificial neuron. Here are the core takeaways:

### 1. The Forward Pass: Making a Prediction

The neuron processes input in two steps:

- **Weighted Sum (Logit):** Each input is multiplied by a learned **weight** (representing importance) and summed with a **bias** (an offset). This produces a raw score, `z`.
  - **Example:** `z = (1.0 × 0.4) + (0.0 × 0.2) + (1.0 × 0.3) - 0.8 = -0.1`

- **Activation Function:** The raw score is passed through a **sigmoid** function, which squashes it into a range between 0 and 1. This output is interpreted as the model's **confidence**.
  - **Example:** `σ(-0.1) ≈ 0.475` (47.5% confidence)

A **threshold** (e.g., 0.5) is then applied to convert this confidence score into a final predicted class (`0` or `1`).

### 2. The Backward Pass: Learning from Error

This is how the model improves:

- **Calculate Loss:** We quantify the error using a loss function, like **squared error**: `Loss = (true_label - predicted_value)²`

- **Calculate Gradients (Backpropagation):** Using calculus (PyTorch's `autograd`), we compute the **gradient** of the loss with respect to each weight. This tells us the direction and magnitude to adjust each weight to reduce the error.

- **Update Weights (Gradient Descent):** Each weight is nudged in the opposite direction of its gradient, scaled by a **learning rate (η)**:
  `new_weight = old_weight - η × gradient`

> **Analogy:** Imagine the loss as a hilly landscape. The gradient points uphill, so we step downhill (opposite direction) to find the lowest point (minimum loss).

### 3. Hyperparameters vs. Learned Parameters

It's crucial to distinguish between what the model **learns** and what we **set**:

| **Learned by Model** | **Set by User (Hyperparameters)** |
| :--- | :--- |
| Weights | Learning Rate (η) |
| Bias | Classification Threshold |
| | Activation Function Choice |
| | Network Architecture |

- **Weights & Bias** are the internal state that changes during training.
- **Hyperparameters** are the "knobs" we tune to control the learning process. A learning rate that is too small means slow learning; too large means the model may never converge.

## Dependencies
The project requires the following Python libraries (all listed in `requirements.txt`):
- `torch` (PyTorch)
- `tensorflow`
- `notebook` (Jupyter)
- `numpy`
- `matplotlib`

## AI Assistance Disclosure
This project was developed with the assistance of AI language models. AI tools were utilized to:
- Generate code scaffolding and boilerplate.
- Debug syntax errors and logical issues.
- Provide explanations of complex mathematical concepts.
- Suggest best practices for code organization and documentation.

All code was rigorously reviewed, tested, and understood by the team members. The conceptual understanding, implementation decisions, and final submissions represent the original work of Group 3.

## Submission Information
- **Course:** Machine Learning Frameworks
- **Assignment:** Single Layer Perceptron Workshop
- **Group:** 3
- **Repository:** https://github.com/ricardo-mohammed/single-layer-perceptron.git
