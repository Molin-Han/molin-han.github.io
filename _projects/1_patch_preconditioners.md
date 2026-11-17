---
layout: page
title: Patch preconditioners
description: Robust multigrid solvers for implicit discretisations of the Boussinesq equations on thin, anisotropic meshes. PhD research, 2024–present.
img: assets/img/projects/patch_preconditioner.png
importance: 1
github: https://github.com/Molin-Han/Boussinesq_implicit
related_publications: true
---

**PhD research, Department of Mathematics, Imperial College London (October 2024 – present).** Supervisor: [Prof. Colin Cotter](https://profiles.imperial.ac.uk/colin.cotter).

Implicit time stepping in ocean and atmosphere models requires the solution of a large, ill-conditioned linear system at every time step. On thin domains, with small aspect ratio, the meshes are severely anisotropic and standard point-smoother preconditioners lose their effectiveness. This project builds preconditioners whose performance does not degrade in that regime.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/patch_preconditioner.png" title="vertical line patch on an anisotropic mesh" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic of a vertical vertex-patch on an anisotropic vertical-slice mesh: the smoother solves on each such column of cells together, so the strong coupling in the vertical direction is captured within a single patch.
</div>

#### Approach

- **Mixed Poisson-type systems.** A shift eliminates the pressure, leaving a grad-div Helmholtz-type problem that is solved by multigrid with additive Schwarz line smoothers.
- **Nonlinear incompressible Boussinesq equations** on a vertical slice. A shifted auxiliary operator isolates the velocity–buoyancy block, which is solved by multigrid with vertical vertex-patch line smoothers that exploit the mesh anisotropy.
- **Choice of shift.** A heuristic shift parameter is replaced by a bound derived from the system linearised about a state of rest.

#### Results

Iteration counts are robust to the aspect ratio and the mesh spacing, and solves are faster than with standard methods. The solver is validated on the Skamarock–Klemp gravity-wave test case in parallel MPI runs on an HPC cluster. A manuscript is in preparation {% cite han2026patch %}.

#### Software

The solvers are written in [Firedrake](https://www.firedrakeproject.org/) and [PETSc](https://petsc.org/), with [Irksome](https://github.com/firedrakeproject/Irksome) automating the auxiliary-operator preconditioner for implicit Runge–Kutta methods. I contributed to Firedrake's additive Schwarz patch preconditioners, `ASMStarPC` and `ASMVankaPC`, in [PR #5211](https://github.com/firedrakeproject/firedrake/pull/5211). Code: [Molin-Han/Boussinesq_implicit](https://github.com/Molin-Han/Boussinesq_implicit).

#### Next steps

Extending the solver to the Lagrangian-averaged Boussinesq (alpha) model and to three dimensions with fully implicit time integration.

#### Talks on this work

- SciCADE 2026, Edinburgh: _Iterative solvers for implicit discretisations of the Boussinesq system via patch-wise preconditioning._
- PETSc Annual User Meeting and Firedrake '26, Oxford: _Robust preconditioning for the Boussinesq equations through patch-wise multigrid smoother._
- Firedrake '25, Leeds: _A robust patch-wise preconditioner for mixed Poisson equations._
