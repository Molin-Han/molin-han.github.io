---
layout: page
title: Bounded DG transport
description: Conservative, bounded discontinuous Galerkin transport with a hierarchical flux limiter, in Firedrake. Undergraduate research (UROP), summer 2022.
img: assets/img/projects/dg_transport.png
importance: 4
github: https://github.com/Molin-Han/Firedrake_DG_transport
---

**Undergraduate Research Opportunities Programme (UROP), Imperial College London (June – September 2022).** Supervisor: [Prof. Colin Cotter](https://profiles.imperial.ac.uk/colin.cotter). Funded by a UROP bursary from the Department of Mathematics.

- Built and simulated transport equations with compressible flow in [Firedrake](https://www.firedrakeproject.org/), using a conservative discontinuous Galerkin discretisation.
- Implemented a hierarchical flux limiter that keeps the advected solutions bounded.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/dg_transport.png" title="advected tracer" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/dg_transport_density.png" title="density" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Snapshots from the project's animations of the advected tracer (left) and the density (right), rendered in ParaView.
</div>

Code: [Molin-Han/Firedrake_DG_transport](https://github.com/Molin-Han/Firedrake_DG_transport).
