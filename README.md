# Hydrostatic Thrust Bearing Design Optimization

This repository contains the implementation of an optimization problem involving the **design of hydrostatic thrust bearings**. The goal is to **minimize power loss** subject to a set of nonlinear constraints.
-------------------
## Problem Overview

Hydrostatic thrust bearings are used in engineering systems where minimizing power loss is critical. This optimization problem is solved by finding the optimal values for:

- `x1 = Q`: flow rate  
- `x2 = R0`: recess radius  
- `x3 = R`: bearing step radius  
- `x4 = µ`: viscosity of the fluid  
----------------------
### Objective Function

The main objective is to minimize:
**f(x) = (P₀(x) · x₁)^0.7 + Eₓ(x)**  
where:
- `P₀(x)` is the inlet pressure
- `x₁` is the flow rate
- `Eₓ(x)` is the friction loss
----------------------

Subject to 7 nonlinear constraints related to:

- Load capacity
- Oil pressure and temperature rise
- Oil film thickness
- Geometry and design limits

(See `Hydrostatic Thrust Bearing Design.pdf` for full equations.)
--------------------------
## Contents

- `Hydrostatic Thrust Bearing Design.ipynb`: Jupyter notebook with full implementation
- `Hydrostatic Thrust Bearing Design.pdf`: Problem description and equations
- `README.md`: Project documentation
-------------------------
## Implemented Methods

Two global optimization methods are implemented from scratch:

1. **Random Search (RS)**
2. **Simulated Annealing (SA)**

Each algorithm:
- Is run 21 times
- Limited to 10,000 function evaluations per run
- Returns the best approximation of the optimal solution `x*`
----------------------------
## Validation

All core functions (`f(x)` and `g1(x)` to `g7(x)`) were implemented independently and tested against a known set of inputs. Function call counters were included for performance tracking.
--------------------------------
## Technologies Used

- Python 3.x
- Jupyter Notebook
- Numpy
- Matplotlib (for visualizations)

-----------------------------------
