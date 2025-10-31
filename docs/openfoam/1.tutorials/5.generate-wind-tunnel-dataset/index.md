---
title: Generate a Wind Tunnel Simulation Dataset
description: ""
seo:
 title: ""
 description: ""
---

In this tutorial, we will demonstrate how to use the Inductiva API to efficiently generate an OpenFOAM dataset 
in parallel by varying the inlet wind speed. This approach allows rapid creation of multiple simulation cases 
with different wind conditions, facilitating the analysis of flow behavior and performance sensitivity over 
a controlled range of wind speeds. By leveraging cloud resources, users can run these simulations in parallel 
and accelerate the generation of CFD data for further study or integration into downstream workflows.

> 📺 **Prefer video?**  
> This guide is also available as a webinar replay, where we walk through running **OpenFOAM on Inductiva** step by step — from setup to dataset generation. [Watch the full demo here](../../4.webinars/1.openfoam-cfd-dataset)

<p align="center"><img src="openfoam/bike_pressure_field.png" alt="OpenFOAM motorBike visualization" width="700"></p>

To demonstrate this process, we will use the incompressible, steady-state simpleFoam solver along with 
the **motorBike example**, which is available in the OpenFOAM repository.

In this tutorial, we'll walk through how to:
- [Review the prerequisites for running the motorBike case](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section1)
- [Run the simulation](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section2)
- [Generalize the use case](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section3)
- [Generate synthetic wind tunnel data at scale](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section4)
- [Postprocessing with Inductiva](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section5)
- [Results and Key Takeaways](/guides/openfoam/tutorials/generate-wind-tunnel-dataset/sections/section6)

::docsbanner
::