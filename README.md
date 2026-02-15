# Numerical-Solutions-of-Differential-Equations-and-Oscillations

Spring-Mass System Simulation: Euler vs Runge-Kutta (RK2)

This project simulates a spring-mass system using numerical integration methods in Python. It compares the performance of the Euler method and the 2nd-order Runge-Kutta (RK2) method for solving the equations of motion.

## 1. Overview

A simple spring-mass system is modeled using Hooke’s law:

!(NUMERICAL IMAGE.png)

where:

𝑚
m = mass (kg)

𝑘
k = spring constant (N/m)

𝑥
x = displacement (m)

Numerical integration methods are used to approximate the motion:

Euler Method – Simple, first-order method

Runge-Kutta 2nd Order (RK2) – More accurate, second-order method

The project visualizes the displacement over time for both methods and compares them.

## 2. Libraries Required
`
import numpy as np
import matplotlib.pyplot as plt
`
## 3. Features

Simulates displacement and velocity over time

Implements Euler and RK2 numerical methods

Compares the accuracy and stability of Euler vs RK2

Generates three plots:

RK2 displacement vs time

Euler displacement vs time

Euler vs RK2 comparison


## 4. Parameters

` m = 1.0 kg` – Mass of the object

`k = 1.0 N/m` – Spring constant

`dt = 0.01 s` – Time step

`x0 = 1.0 m` – Initial displacement

`v0 = 0.0 m/s` – Initial velocity

Simulation duration: 0 – 20 seconds


Author Katlego Mathebula
