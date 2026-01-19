# Assignment Optimization Model

This repository contains a **simple assignment optimization model** implemented in Python using **PuLP** with the free **CBC solver**.

The model assigns each worker to exactly one job (and one job to exactly one worker) while minimizing total assignment cost.  
The implementation is provided in a **Jupyter notebook**.

---

## Problem Overview

Given:
- A set of workers
- A set of jobs
- A cost for assigning each worker to each job

The goal is to find the minimum-cost assignment such that:
- Each worker is assigned to exactly one job
- Each job is assigned to exactly one worker

---

## Mathematical Formulation

**Decision Variable**

\[
x_{w,j} =
\begin{cases}
1 & \text{if worker } w \text{ is assigned to job } j \\
0 & \text{otherwise}
\end{cases}
\]

**Objective**

\[
\min \sum_{w}\sum_{j} c_{w,j} \, x_{w,j}
\]

**Constraints**
- Each worker is assigned to exactly one job  
- Each job is assigned to exactly one worker  
- Binary decision variables  

---

## Implementation Details

- Language: Python  
- Optimization library: PuLP  
- Solver: CBC (open-source, free)  
- Environment: Jupyter Notebook  

The base implementation solves a **square assignment problem**
(number of workers equals number of jobs).

---

## Repository Structure

.
├── assignment.ipynb # The Jupyter notebook with the assignment model
└── README.md



---

## How to Run

1. Install dependencies:
   ```bash
   pip install pulp

