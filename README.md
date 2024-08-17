# Non-Linear Modeling with MLP

## Overview

This project explores the use of a Multi-Layer Perceptron (MLP) to model a non-linear relationship between independent and dependent variables in a dataset. The dataset contains 500 rows, each with two independent variables and one dependent variable. The project investigates whether the problem is one of regression or classification and determines the optimal learning rate for training the MLP.

## Problem Statement

### 1. Problem Type Determination

Upon investigating the dataset, it was determined that the problem is one of **regression**. The dependent variable is continuous, and the goal is to predict this variable based on the values of the two independent variables.

**Justification**:
- The dependent variable represents a continuous value, making it suitable for regression modeling rather than classification.

### 2. Model Selection: Multi-Layer Perceptron (MLP)

Given the non-linear nature of the relationship between the independent variables and the dependent variable, a Multi-Layer Perceptron (MLP) was selected for the task. The model was implemented using `scikit-learn`'s `MLPRegressor`.

### 3. Learning Rate Selection Methodology

The learning rate is a critical hyperparameter that determines the size of the steps taken when updating the model's weights during training. To select an appropriate learning rate, the following methodology was employed:

- The `learning_rate` parameter was set to `'constant'`, and the `learning_rate_init` was varied across a range of values.
- The model's performance was evaluated based on:
  - Training loss
  - Convergence behavior
  - Generalization to unseen data (cross-validation)
- Graphs were produced to visualize the effect of different learning rates on model performance.

### 4. Final Learning Rate Choice

After conducting experiments with various learning rates, the optimal learning rate was found to be **0.2**. This rate provided a good balance between convergence speed and stability, resulting in effective training without oscillations or divergence.

### 5. Model Training and Evaluation

The MLP was trained using the selected learning rate of 0.01. The model's performance was evaluated using the coefficient of determination (R² score) to assess how well the model captured the variance in the dependent variable.

**Results**:
- The coefficient of determination (R² score) for the trained model was **0.977**, indicating that the model explains 97% of the variance in the dependent variable. And an MSE Score of **76.05**

**Conclusion**
This project demonstrates the process of determining the type of problem, selecting an appropriate model (MLP), and tuning a critical hyperparameter (learning rate) for optimal performance in modeling a non-linear relationship. The final model achieved a good R² score, indicating strong predictive performance.
