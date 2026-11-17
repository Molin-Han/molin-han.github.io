---
layout: about
title: about
permalink: /
subtitle: PhD student in computational mathematics, <a href='https://www.imperial.ac.uk/mathematics/'>Department of Mathematics</a>, <a href='https://www.imperial.ac.uk/'>Imperial College London</a>

profile:
  align: right
  image: prof_pic.jpg # replace assets/img/prof_pic.jpg with your own photo
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Department of Mathematics</p>
    <p>Imperial College London</p>
    <p>London SW7 2AZ, UK</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
---

I am a third-year PhD student in mathematics at Imperial College London, supervised by [Prof. Colin Cotter](https://profiles.imperial.ac.uk/colin.cotter). I hold a President's PhD Scholarship and am aligned with the EPSRC Centre for Doctoral Training in [Mathematics for our Future Climate](http://mfccdt.ac.uk/).

My research is on fast, robust solvers for implicit time stepping in ocean and atmosphere models. Implicit methods need the solution of a large, ill-conditioned linear system at every time step, and on thin domains, where the meshes are strongly anisotropic, standard point-smoother preconditioners lose their effectiveness. I design patch-based multigrid preconditioners for the incompressible Boussinesq equations whose iteration counts stay robust to the aspect ratio and the mesh spacing, and implement them as parallel code in [Firedrake](https://www.firedrakeproject.org/) and [PETSc](https://petsc.org/). I am now extending this work to the Lagrangian-averaged Boussinesq (alpha) model and to three dimensions.

Before the PhD I took an MSci in Mathematics at Imperial with First Class Honours. Along the way I worked on parallel-in-time preconditioning for optimal control of the wave equation, matrix-free solvers for thermoacoustic stability analysis at the Technical University of Munich, and bounded discontinuous Galerkin transport for atmospheric flows.

**Research interests:** finite element methods, numerical linear algebra and preconditioning, geophysical fluid dynamics, high-performance computing.

Outside research I enjoy hiking, tennis, astrophotography and calligraphy.
