---
title: "Scientific programming languages"
subtitle: Thank you for reading my blog. This article is dedicated to scientific programming languages.

# Summary for listings and search engines
summary: Thank you for reading my blog. This article is dedicated to scientific programming languages.

# Link this post with a project
projects: []

# Date published
date: '2023-05-06T00:55:00Z'

# Date updated
lastmod: '2023-05-06T00:55:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named featured.jpg/png in this page's folder and customize its options here.
image:
  caption: 'Image credit: **Deibatulina** (https://deibatulina.github.io)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - cpp
  - python
  - maple
  - matlab
  - fortran

categories:
  - Demo
---

## Scientific programming languages

  In computer programming, a scientific programming language can refer to two degrees of the same concept.

  In a broad sense, a scientific programming language is a programming language that is widely used for computational science and computational mathematics. In this sense, C/C++ and Python can be considered scientific programming languages.

  In a broader sense, a scientific programming language is one that is designed and optimized to use mathematical formulas and matrices. Such languages are characterized not only by the presence of libraries that perform mathematical or scientific functions, but also by the syntax of the language itself. For example, neither C++ nor Python have built-in matrix types or functions for matrix arithmetic (addition, multiplication, etc.); instead, this functionality becomes available through standard libraries. Scientific programming languages in a broader sense include ALGOL, APL, Fortran, J, Julia, Maple, MATLAB and R.

  Scientific programming languages should not be confused with scientific language in general, which in a broad sense denotes higher standards of accuracy, correctness and conciseness expected from practitioners of the scientific method.

## Examples

### Linear algebra

  Scientific programming languages provide tools for working with linear algebra. For example, the following program in the Julia scientific programming language solves a system of linear equations:

```
A = rand(20, 20)  # A - матрица 20x20
b = rand(20)      # b - вектор из 20 элементов
x = A\b           # x - решение A * x = b
```

Working with large vectors and matrices is a key feature of these languages, as linear algebra lays the foundation for mathematical optimization, which in turn provides basic applications such as deep learning.
  
### Mathematical optimization

  In a scientific programming language, we can calculate the optimum of functions with a syntax close to a mathematical language. For example, the following Julia code finds the minimum of a polynomial

$$ P(x,y)=x^2-3*x*y+5*y^2-7*y+3. $$

```
использование Optim

P(x,y) = x^2 - 3x*y + 5y^2 - 7y + 3

z₀ = [ 0.0
       0.0 ]     

optimize(z -> P(z...), z₀, Newton();
         )
```

  This example uses Newton's method to minimize. Modern scientific programming languages will use automatic differentiation to calculate gradients and hash values of a function given as input; cf. differentiable programming. Here automatic direct differentiation was chosen for this task. Old scientific programming languages, such as the venerable Fortran, would require the programmer to pass next to the optimized function a function that calculates the gradient and a function that calculates the Hessian.

  With more knowledge of the function to be minimized, more efficient algorithms can be used. For example, convex optimization provides faster calculations when the function is convex, quadratic programming provides faster calculations when the function is maximally quadratic in its variables, and linear programming when the function is maximally linear.

