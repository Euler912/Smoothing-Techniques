# Smoothing Methodologies for Non-Differentiable Optimization

## Project Overview
This repository serves as a centralized hub for researching and implementing advanced smoothing techniques for non-smooth functions. The primary objective is to approximate **non-differentiable max functions** with smooth, differentiable surrogates.

These methodologies are critical components in both **Non-Convex Optimization** and **Convex Robust Optimization**. By transforming "sharp" functions into well-behaved, differentiable surfaces, we enable the use of efficient gradient-based algorithms to solve complex problems that are otherwise mathematically intractable.

## Main Objective: Smoothing the Max Function
In optimization, the `max` function is often used to represent the worst-case scenario or to aggregate multiple constraints. However, its non-differentiability at intersection points prevents the direct application of standard first- and second-order methods. 

By applying **Moreau-Yosida** and **KS smoothing**, we can handle:
* **Convex Robust Optimization**: Providing smooth approximations for worst-case designs where the objective is a maximum over a set of scenarios.
* **Non-Convex Optimization**: Navigating complex landscapes by rounding off kinks and providing tightness guarantees for global solutions.

---

## Repository Structure

### 1. Moreau-Yosida Regularization
Located in the `/Moreau-Yosida` sub-directory.
* **Concept**: Uses the **Moreau envelope** to regularize non-smooth functions. It drops a quadratic "bowl" into sharp corners, creating a perfectly smooth transition.
* **Application**: Turning non-differentiable problems into smooth ones to allow high-speed gradient-based solvers.



### 2. Kreisselmeier-Steinhauser (KS) Smoothing
Located in the `/KS-Smoothing` sub-directory.
* **Concept**: An aggregation technique that uses an exponential-sum-log approach to follow the "envelope" of multiple functions.
* **Application**: Collapsing a massive pile of different constraints or scenarios into a single, well-behaved smooth function—ideal for robust engineering and design.



---

## Academic Context
These implementations are part of a broader research effort into obtaining guarantees on the **tightness of global solutions** in non-convex optimization, supervised by Prof. Aharon Ben-Tal at the Technion.

## Tech Stack
* **Language**: Python
* **Core Libraries**: NumPy, SciPy
* **Visualization**: Matplotlib
