---
layout: page
title: Thermoacoustic solvers
description: Matrix-free Newton and eigenvalue solvers, and how conditioning affects GMRES. Visiting research student at TU Munich, summer 2023.
img: assets/img/projects/thermoacoustics.png
importance: 3
---

**Visiting research student, TUM PREP, Technical University of Munich (July – September 2023).** Supervisors: Prof. Wolfgang Polifke and Philipp Brokof, Mechanical Engineering. Fully funded by the Turing Scheme and the Bavarian State Ministry of Education, Science and the Arts.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/thermoacoustics.png" title="thermoacoustic feedback in a duct" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic of thermoacoustic feedback: unsteady heat release from a flame couples to the acoustic modes of the duct that contains it.
</div>

- Implemented matrix-free versions of a Newton solver and an eigenvalue solver for thermoacoustic stability analysis.
- Analysed how the condition number affects the convergence of GMRES for heat equations and for the nonlinear Navier–Stokes equations in thermoacoustics.
- Presented the results in a twenty-minute talk to the research group.
