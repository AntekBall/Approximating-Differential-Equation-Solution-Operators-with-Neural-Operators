# Approximating Differential Equation Solution Operators with Neural Operators

Master thesis at SGH exploring **Neural Operators** (such as Fourier Neural Operators and DeepONets) to learn mapping between infinite-dimensional function spaces. This repository focuses on approximating solution operators for both Ordinary Differential Equations (ODEs) and Partial Differential Equations (PDEs).

## 📌 Overview

Traditional numerical methods (e.g., Finite Element, Finite Difference) compute solutions to differential equations for a single instance of boundary/initial conditions or parameters. When parameters change, the full system of equations must be solved again from scratch. 

**Neural Operators** overcome this limitation by learning the entire *solution operator*, a mapping between infinite-dimensional function spaces.

Key benefits include:

* **Discretization Invariance:** Train on lower-resolution spatial grids and perform zero-shot evaluation on arbitrarily higher resolutions without retraining.
* **Fast Inference:** Once trained, generating a new solution takes milliseconds compared to seconds or minutes with traditional solvers.
* **Data-Driven & Physics-Informed Flexibility:** Learn operators directly from simulation datasets or incorporate PDE residuals into loss functions.

## 🛠️ Features & Methods

* **Neural Operator Architectures:**
  * **Fourier Neural Operator (FNO):** Parameterizes integral kernels directly in Fourier space via Fast Fourier Transforms (FFT) for global context modeling.
  * **Deep Operator Network (DeepONet):** Utilizes separate Branch (input functions) and Trunk (evaluation domain coordinates) networks based on the Universal Approximation Theorem for operators.
* **Benchmark Differential Equations:**
  * Logistic Growth 
  * RCK growth model
  * Burgers Equation


