Feature Engineering and Polynomial Regression Lab

GitHub Repository: https://github.com/Feature-Engineering-and-Polynomial-Regression

This repository contains an optional lab exploring Feature Engineering and Polynomial Regression using Python, NumPy, and Matplotlib. The lab demonstrates how linear regression can be extended to model complex, non-linear functions by transforming input features.

Table of Contents
Introduction

Goals

Tools

Feature Engineering and Polynomial Regression Overview

Polynomial Features

Selecting Features

Feature Scaling

Complex Functions

Conclusion

Introduction
Out-of-the-box, linear regression is designed to build models of the form:

f 
w,b
​
 =w 
0
​
 x 
0
​
 +w 
1
​
 x 
1
​
 +...+w 
n−1
​
 x 
n−1
​
 +b(1)
However, real-world data often exhibits non-linear relationships. This lab addresses the challenge of fitting non-linear curves using the existing linear regression machinery. It shows how feature engineering—the process of creating new features from existing ones—can transform non-linear data into a format suitable for linear regression.

For example, housing prices might not be linearly related to living area; instead, they might penalize very small or very large houses, resulting in a curved relationship. This lab demonstrates how to handle such scenarios.

Goals
In this lab, you will:

Explore feature engineering and polynomial regression, enabling the use of linear regression to fit very complicated, even highly non-linear functions.

Recognize the importance of applying feature scaling when performing feature engineering.

Tools
You will utilize functions developed in previous labs, as well as matplotlib for plotting and NumPy for numerical operations. The core utility functions (zscore_normalize_features, run_gradient_descent_feng) are assumed to be available from lab_utils_multi.py.

Feature Engineering and Polynomial Regression Overview
The lab begins by illustrating a scenario where standard linear regression fails to fit a non-linear curve (e.g., y=1+x 
2
 ). It then introduces the concept of polynomial features to address this limitation.

Polynomial Features
This section demonstrates how to engineer new features by transforming the input data. For a quadratic relationship like y=1+x 
2
 , simply replacing the original input x with x**2 allows a linear regression model to achieve a near-perfect fit. The notebook shows the results of gradient descent successfully finding parameters close to the target function.

Selecting Features
The lab further explores scenarios where the required features might not be immediately obvious. It provides an example of trying multiple polynomial features (e.g., x, x 
2
 , x 
3
 ) and observing how gradient descent adjusts the weights for each feature.

Feature Scaling
A crucial aspect highlighted in the lab is the importance of feature scaling when using polynomial features. When features are engineered (e.g., x, x 
2
 , x 
3
 ), their magnitudes can vary significantly. This can lead to issues with gradient descent, such as slow convergence or oscillations. The zscore_normalize_features function is used to normalize these features, ensuring that gradient descent performs effectively.

Complex Functions
The lab extends the concept to more complex non-linear functions, such as y=
cos(x/2). It demonstrates how a higher degree of polynomial features (e.g., up to x 
13
 ) combined with feature scaling can enable linear regression to approximate such intricate relationships.

Conclusion
In this lab, you:

Learned how linear regression can model complex, even highly non-linear functions using feature engineering.

Recognized that it is important to apply feature scaling when doing feature engineering.
