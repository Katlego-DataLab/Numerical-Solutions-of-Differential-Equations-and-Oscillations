# Numerical Simulation of Oscillatory Systems

## Euler vs Runge-Kutta (RK2) for a Spring-Mass System

**Author:** Katlego Mathebula
**Tech Stack:** Python · NumPy · Matplotlib
**Project Type:** Numerical Methods & Differential Equations


## Executive Summary

This project implements and compares two numerical integration techniques,  the **Euler Method** and the **2nd-Order Runge-Kutta (RK2)** method, to solve the second-order differential equation governing a simple spring-mass system.

The goal is to evaluate:

- Accuracy
- Stability
- Error propagation
- Long-term oscillatory behavior

This project demonstrates how numerical methods approximate physical systems and highlights the importance of method selection in scientific computing.


## Physical System Modeled

The system follows Hooke’s Law:

$$
m \frac{d^2x}{dt^2} + kx = 0
$$

Where:

- ( m ) = mass (kg)
- ( k ) = spring constant (N/m)
- ( x(t) ) = displacement

This represents a **simple harmonic oscillator**.

The analytical solution is sinusoidal motion with angular frequency:

$$
\omega = \sqrt{\frac{k}{m}}
$$

Since exact solutions are known, this system is ideal for testing numerical method performance.



## Conversion to First-Order System

To apply numerical methods, the second-order ODE is converted into two first-order equations:
$$
\frac{dx}{dt} = v
$$

$$
\frac{dv}{dt} = -\frac{k}{m}x
$$

This allows iterative time-stepping solutions.


## Numerical Methods Implemented

### 1. Euler Method (First-Order)

The Euler method updates position and velocity using:
$$
x_{n+1} = x_n + dt \cdot v_n
$$

$$
v_{n+1} = v_n - dt \cdot \frac{k}{m}x_n
$$

Characteristics:

- First-order accuracy
- Global error: (O(dt))
- Simple but prone to instability
- Accumulates energy error over time


### 2. Runge-Kutta 2nd Order (RK2)

RK2 improves accuracy using midpoint-style slope estimation:

$$
x_{n+1} = x_n + \frac{dt}{2}(k_1 + k_2)
$$

$$
v_{n+1} = v_n + \frac{dt}{2}(l_1 + l_2)
$$
Characteristics:

- Second-order accuracy
- Global error: (O(dt^2))
- Better stability
- Reduced phase drift
- Improved energy conservation

## Simulation Parameters

- Mass ( m = 1.0 ) kg
- Spring constant ( k = 1.0 ) N/m
- Time step ( dt = 0.01 ) s
- Initial displacement ( x_0 = 1.0 ) m
- Initial velocity ( v_0 = 0.0 ) m/s
- Simulation duration: 0 – 20 seconds


## Results & Observations

### RK2 Method

- Produces stable sinusoidal oscillations
- Preserves amplitude more effectively
- Maintains phase consistency over time

### Euler Method

- Shows amplitude growth (energy drift)
- Accumulates numerical error
- Becomes unstable over long simulation times

### Direct Comparison

When plotted together:

- RK2 closely approximates expected harmonic motion
- Euler gradually diverges from the physical solution

This illustrates how lower-order methods introduce systematic error in oscillatory systems.


## Numerical Stability Analysis

For oscillatory systems:

- Euler is conditionally stable
- Small time steps reduce error but increase computation cost
- RK2 allows better accuracy at a similar time step

This demonstrates the tradeoff between:

- Computational efficiency
- Accuracy
- Stability

These considerations are critical in:

- Engineering simulations
- Computational physics
- Control systems
- Aerospace modeling
- Structural analysis

## Why This Project Matters

This project demonstrates:

* Understanding of second-order differential equations
* Conversion to first-order systems
* Implementation of iterative solvers
* Error order analysis
* Stability considerations
* Physical interpretation of numerical results

It bridges mathematics, physics, and computational implementation.

## Libraries Used

```python
import numpy as np
import matplotlib.pyplot as plt
```

- NumPy → Numerical computation
- Matplotlib → Visualization

## Potential Extensions

To deepen analysis:

- Compare with analytical solution
-  Compute global error norms
- Implement the RK4 method
- Perform time-step sensitivity analysis
- Analyze energy conservation numerically
- Extend to damped or forced oscillators


## Conclusion

This project highlights how numerical methods approximate physical systems and why higher-order integrators are often preferred for oscillatory dynamics.

The comparison between Euler and RK2 clearly demonstrates:

- Error accumulation
- Stability differences
- Accuracy improvements

It provides foundational insight into computational modeling of dynamical systems.




You are building serious mathematical depth now.
