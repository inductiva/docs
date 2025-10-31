---
title: Run occDrivAerStaticMesh from the OpenFOAM HPC Benchmark Suite
description: ""
seo:
 title: ""
 description: ""
---

The **occDrivAerStaticMesh simulation** focuses on the open-closed cooling (occ) variant of the DrivAer model -
an industrially relevant benchmark case that represents a full-scale passenger vehicle with static wheels and sealed cooling inlets.

The geometry is derived from the notchback version of the **Ford Open Cooling DrivAer (OCDA) model** and features a highly
detailed underbody and engine bay configuration, adding significant complexity compared to the original DrivAer design.

As part of the *2025 OpenFOAM HPC Challenge*, the model was adapted for steady-state
RANS simulations using the SIMPLE algorithm with fixed inner iterations. To support compatibility and scalability in
high-performance computing environments, pre-generated meshes at multiple resolutions are provided, enabling robust and
reproducible simulations.

In this tutorial, we'll walk through how to:
- [Review the prerequisites for running the occDrivAerStaticMesh case](/guides/openfoam/tutorials/run-occdrivaerstaticmesh-case/section1)
- [Run the simulation on a single-machine](/guides/openfoam/tutorials/run-occdrivaerstaticmesh-case/section2)
- [Prepare the simulation for execution on an MPI cluster](/guides/openfoam/tutorials/run-occdrivaerstaticmesh-case/section3)
- [Scale the simulation across multiple machines](/guides/openfoam/tutorials/run-occdrivaerstaticmesh-case/section4)

This guide is divided into a few straightforward steps. Follow along to explore the performance and scalability of this simulation
using the **Inductiva API**.

👉 Check out our [blog post](https://inductiva.ai/blog/article/from-supercomputer-to-cloud-a-new-era-for-openfoam-simulations) for the full story.

::docsbanner
::

