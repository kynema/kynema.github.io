=======================
 Kynema Software Stack
=======================

.. note::
    
    This website is in active development; further details are in the process of being added.

*insert background of Kynema tools and list directives*

Open-source tools
-----------------

**Kynema-SGF** (formerly AMR-Wind):
`Repository <https://github.com/Kynema/kynema-sgf>`__ |
`Documentation <https://kynema.github.io/kynema-sgf>`__

.. collapse:: Description

    A massively parallel, block-structured adaptive-mesh, incompressible flow solver. The solver is built on top of the AMReX library, and the SGF suffix stands for structured-grid fluid dynamics.
    The primary applications for Kynema-SGF are: performing large-eddy simulations (LES) of atmospheric boundary layer (ABL) flows, simulating wind farm turbine-wake interactions using actuator disk or actuator line models for turbines, and as a background solver when coupled with a near-body solver (e.g., Kynema-UGF) with overset methodology to perform blade-resolved simulations of multiple wind turbines within a wind farm. For offshore applications, the ability to model the air-sea interaction effects and its impact on the ABL characteristics is another focus for the code development effort.

|

**Kynema-UGF** (formerly Nalu-Wind):
`Repository <https://github.com/Kynema/kynema-ugf>`__ |
`Documentation <https://kynema.github.io/kynema-ugf>`__

.. collapse:: Description

    A generalized, unstructured-grid, massively parallel, incompressible-flow solver. The solver is primarily built upon the packages provided by the Trilinos project, and the suffix UGF stands for unstructured-grid fluid dynamics.
    When coupled to a background solver (e.g., Kynema-SGF) with overset methodology,
    Kynema-UGF serves as a near-body solver to perform geometry-resolved simulations
    of fluid-structure interactions.

|

**Kynema driver:**
`Repository <https://github.com/Kynema/kynema-driver>`__

.. collapse:: Description

    The driver of the hybrid Kynema solver, which combines Kynema-SGF and Kynema-UGF in an overset framework.

|

**Kynema manager:**
`Repository <https://github.com/Kynema/kynema-manager>`__ |
`Documentation <https://kynema.github.io/kynema-manager>`__

.. collapse:: Description

    A project specialization of Spack-Manager. Spack-Manager is a light-weight extension to Spack that is intended to streamline the software development and deployment cycle for software projects on specific machines. A given software project, especially in high performance computing (HPC), typically requires managing multiple software dependencies using multiple compilers and processing devices across many machines. Spack-Manager is quite literal in its name, in that it provides a way to manage and organize these configurations across multiple machines, and multiple projects. Kynema-Manager is specialized towards the Kynema project, which is a set of complex coupled applications for modeling the physics of entire wind farms at high fidelities. However, much of what Kynema-Manager accomplishes is merely an example of how Spack-Manager can be specialized towards any single project or projects.

|

**Kynema benchmarks:**
`Repository <https://github.com/Kynema/kynema-benchmarks>`__ |
`Website <https://kynema.github.io/kynema-benchmarks>`__

|

**AMR-Wind frontend:** (not yet updated to current naming convention)
`Repository <https://github.com/Exawind/amr-wind-frontend>`__ |
`Documentation <https://github.com/Exawind/amr-wind-frontend/blob/main/docs/README.md>`__

.. collapse:: Description

    A tool to help setup, visualize, and postprocess AMR-Wind simulations. Built
    using the TK yaml library. It can:

    - Load an AMR-Wind input file and change parameters interactively
    - Plot the simulation domain, including refinement zones and sampling probes/planes
    - Help visualize the sampling outputs (probes, lines, and planes)
    - Help postprocess ABL statistics files.
    - Use it in Jupyter notebooks or python scripts to automate processing.

|

Capabilities
------------


Publications
------------


Standards
---------

.. toctree::
   :maxdepth: 2

   standards/developer_glossary