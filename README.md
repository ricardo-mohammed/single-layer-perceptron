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

### 2. Create and Activate Virtual Environment

**Windows:**
```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS/Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies
```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

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

## 💬 Discussion Talking Points

As a group, we explored the foundational mechanics of Artificial Neural Networks through the lens of the Single Layer Perceptron. Here are our key takeaways and talking points from the workshop:

* **The Perceptron as a Decision Maker:** A single neuron mimics biological decision-making by calculating a weighted sum of its inputs, adding a bias, and passing the result through an activation function (like the Step or Sigmoid function). This allows the model to output a clear binary decision or a probability score.
* **The Power of Inhibition (Negative Weights):** We learned that weights don't just amplify signals; they can also inhibit them. By assigning a negative weight to a specific input (e.g., a "long queue" at Canada's Wonderland), the perceptron can effectively model complex logic gates, such as "A AND NOT B".
* **How Machines "Learn" (Error & Weight Updates):** The core of the perceptron learning algorithm lies in its error calculation ($E = y - \hat{y}$). By comparing the predicted output to the actual label, the network calculates the error and updates its weights proportionally. This iterative process allows the model to gradually minimize its loss and improve its accuracy over time.
* **Real-World Application (Canada's Wonderland Case Study):** We successfully translated a qualitative, real-world scenario (deciding whether to go to an amusement park based on weather, queue length, and health) into a quantitative mathematical model. This highlighted how machine learning requires us to carefully engineer and binarize real-world features before feeding them into a network.

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
