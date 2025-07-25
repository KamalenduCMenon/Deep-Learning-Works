# Neural Network Fundamentals and Optimization Techniques


This repository contains two projects that explore foundational neural network concepts and optimization techniques:

- **Backpropagation:** Manual vs Automatic Gradient Computation  
- **Study of Dropout and Batch Normalization in Classifiers**


## Project 1: Backpropagation – Manual vs Autograd

### Overview  
This project demonstrates the backpropagation algorithm by manually calculating gradients and verifying them against PyTorch’s automatic differentiation.

### Problem Statement  
Given input matrices `A`, `B`, `C` and an input vector `x`, the goal is to compute the loss  
\( L = \|C(u + Bx)\|^2 \) where \( u = \sigma(Ax) \),  
and calculate gradients of \( L \) with respect to `A`, `B`, and `C`.

### Methodology  
- Forward propagation with matrix multiplications and sigmoid activation.  
- Manual gradient calculation via chain rule.  
- Verification using PyTorch Autograd.  
- Gradient descent weight update.

### Results and Observations  

| Model   | Dropout | Batch Normalization | Effect Summary                                      |
|---------|---------|---------------------|----------------------------------------------------|
| Softmax | ✔️      | ✔️                  | Dropout reduces overfitting; BatchNorm improves stability and convergence speed. |
| MLP     | ✔️      | ✔️                  | Dropout enhances generalization; BatchNorm accelerates training.                 |
| CNN     | ✔️      | ✔️                  | Both techniques improve robustness and reduce overfitting.                      |


### Technologies  
Python, NumPy, PyTorch


## Project 2: Study of Dropout and Batch Normalization in Classifiers

### Overview  
This project investigates the impact of dropout and batch normalization on the performance of different classifiers on the MNIST dataset.

### Classifiers Implemented  
- Softmax Classifier  
- Multilayer Perceptron (MLP) Classifier  
- Convolutional Neural Network (CNN) Classifier

### Methodology  
- Training each classifier under three conditions: baseline, with dropout, with batch normalization.  
- Dropout rate set at 0.5 to regularize and prevent overfitting.  
- Batch normalization applied to improve training stability and speed.

### Results and Observations  
- Dropout improves generalization by reducing overfitting.  
- Batch normalization accelerates convergence and stabilizes training.  
- Combination of both often yields the best results.

### Technologies  
Python, TensorFlow/Keras, MNIST Dataset


## References

- [Backpropagation - Brilliant](https://brilliant.org/wiki/backpropagation)  
- [How Backward Propagation Works - Analytics Vidhya](https://www.analyticsvidhya.com/blog/2021/06/how-does-backward-propagation-work-in-neural-networks/)  
- [TensorFlow CNN Tutorial](https://www.tensorflow.org/tutorials/images/cnn)  
- [Dropout in Neural Networks - Towards Data Science](https://towardsdatascience.com/dropout-in-neural-networks-47a162d621d9)  
- [Batch Normalization Introduction - Analytics Vidhya](https://www.analyticsvidhya.com/blog/2021/03/introduction-to-batch-normalization/)






