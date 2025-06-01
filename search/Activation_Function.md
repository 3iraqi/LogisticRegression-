# Types of Activation Functions

## Linear Activation Function

- Definition: $f(x) = x$
- Characteristics: Direct mapping, limited in non-linear modeling.
- Use Cases: Rarely used in hidden layers, but can be used in output layers for regression tasks.
- Example: Output layer in linear regression.
- **Pros**: Simple, easy to compute.
- **Cons**: Cannot capture complex patterns, leads to vanishing gradient problem in deep networks.

## Sigmoid Activation Function

- Definition: $f(x) = \frac{1}{1 + e^{-x}}$
- Characteristics: Maps input to range (0, 1), smooth gradient, prone to vanishing gradient problem.
- Use Cases: Binary classification, output layer in logistic regression.
- Example: Output layer in binary classification tasks.
- **Advantages**: Simple and interpretable, good for binary outputs.
- **Disadvantages**: Prone to vanishing gradient problem, especially for very high or low inputs.

## Hyperbolic Tangent (Tanh) Activation Function

- Definition: $f(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
- Characteristics: Maps input to range (-1, 1), zero-centered, mitigates vanishing gradient problem compared to sigmoid.
- Use Cases: Hidden layers in neural networks, especially when zero-centered output is beneficial.
- Example: Hidden layers in feedforward neural networks.
- **Advantages**: Better than sigmoid for hidden layers due to zero-centered output.
- **Disadvantages**: Still suffers from vanishing gradient problem for very high or low inputs.
  
## Rectified Linear Unit (ReLU) Activation Function

- Definition: $f(x) = \max(0, x)$
- Characteristics: Non-linear, outputs zero for negative inputs, linear for positive inputs.
- Use Cases: Widely used in hidden layers of deep neural networks.
- Example: Hidden layers in convolutional neural networks (CNNs).
- **Advantages**: Computationally efficient, mitigates vanishing gradient problem for positive inputs.
- **Disadvantages**: Can suffer from "dying ReLU" problem where neurons can become inactive and stop learning if they output zero for all inputs.
  
## Leaky ReLU Activation Function

- Definition: $f(x) = \max(0.01x, x)$
- Characteristics: Variant of ReLU that allows a small, non-zero gradient when the input is negative.
- Use Cases: Hidden layers in deep neural networks, especially when "dying ReLU" is a concern.
- Example: Hidden layers in deep neural networks.
- **Advantages**: Mitigates "dying ReLU" problem, allows for some gradient flow when inputs are negative.
- **Disadvantages**: Still not zero-centered, can lead to suboptimal performance in some cases.

## Softmax Activation Function

- Definition: $f(x_i) = \frac{e^{x_i}}{\sum_{j} e^{x_j}}$ for each class $i$
- Characteristics: Converts logits into probabilities, outputs sum to 1, used in multi-class classification.
- Use Cases: Output layer in multi-class classification tasks.
- Example: Output layer in neural networks for multi-class classification.
- **Advantages**: Provides a probabilistic interpretation, useful for multi-class classification.
- **Disadvantages**: Sensitive to outliers, can lead to numerical instability if inputs are very large or very small.
