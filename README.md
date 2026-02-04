# Neural Logic Gates from Scratch 

A pure Python implementation of fundamental logic gates using Neural Networks. This project explores the transition from simple linear classifiers to Multi-Layer Perceptrons (MLP) capable of solving non-linear problems.

##  Project Overview

Modern deep learning libraries often abstract away the "gears" of a neural network. This repository aims to demystify the process by building:
1. **Single-Layer Perceptrons (SLP):** To solve linearly separable gates (AND, OR, NAND, NOR).
2. **Multi-Layer Perceptrons (MLP):** To solve non-linear problems (XOR, XNOR) using a hidden layer and backpropagation.

---

##  Mathematical Background

### The Linear Separability Problem
Standard gates like **AND** and **OR** can be separated by a single linear decision boundary. However, **XOR** and **XNOR** cannot. 



To solve this, we utilize:
- **Sigmoid Activation Function:** $\sigma(x) = \frac{1}{1 + e^{-x}}$
- **Backpropagation:** A method used to calculate the gradient of the loss function with respect to the weights by the chain rule.



---

##  Key Features

- **No Libraries:** Built using only Python's standard `math` and `random` modules.
- **Backpropagation Implementation:** Manual calculation of derivatives for weight updates.
- **Error Tracking:** Displays training error convergence for all gates.
- **Modular Design:** Easy to understand and extend.

##  File Structure

- `logic_gates.py`: The main script containing the SLP and MLP classes and training logic.
- `README.md`: Project documentation.

##  Implementation Highlights

### Single-Layer Perceptron (SLP)
Used for basic gates. It uses a simple Step Function to determine the output.


### Multi-Layer Perceptron (MLP)
Used for XOR/XNOR. 
- **Hidden Layer:** 2 Neurons
- **Output Layer:** 1 Neuron
- **Learning Rate:** 0.5
- **Epochs:** 10,000

##  Expected Output

Upon running the script, the network will display final predictions and the average error.
```text
--- SLP Results ---
AND Gate:  [0, 0, 0, 1]
OR Gate:   [0, 1, 1, 1]
NAND Gate: [1, 1, 1, 0]
NOR Gate:  [1, 0, 0, 0]

--- MLP Results ---
XOR Final Error: 0.00042
XOR Predictions: [0, 1, 1, 0]
XNOR Final Error: 0.00038
XNOR Predictions: [1, 0, 0, 1]
