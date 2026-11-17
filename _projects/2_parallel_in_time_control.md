---
layout: page
title: Parallel-in-time optimal control
description: A diagonalisation-based (ParaDiag) preconditioner for the all-at-once optimality system. MSci research project, 2023–24.
img: assets/img/projects/paradiag.png
importance: 2
github: https://github.com/Molin-Han/Optimal_Control_ParaDiag
---

**MSci research project, Imperial College London (October 2023 – June 2024).** Supervisor: [Prof. Colin Cotter](https://profiles.imperial.ac.uk/colin.cotter).

Discretising the optimality system of an optimal control problem for the wave equation, with an all-at-once second-order finite difference scheme in time and P1 finite elements in space, gives one large sparse linear system that couples every time step. The project designed a preconditioner for iterative solution of this system that can be applied in parallel across time, using a unitary diagonalisation in the ParaDiag framework.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/paradiag.png" title="block-circulant structure and its diagonalisation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic of the ParaDiag idea: a block-circulant matrix in time is diagonalised by a discrete Fourier transform, which decouples it into independent problems, one per frequency, that can be solved in parallel.
</div>

The preconditioner was implemented in [Firedrake](https://www.firedrakeproject.org/), and its performance and the accuracy of the solution were demonstrated on a one-dimensional test problem. Code: [Molin-Han/Optimal_Control_ParaDiag](https://github.com/Molin-Han/Optimal_Control_ParaDiag).
