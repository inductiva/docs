---
title: Run 50 simulations in parallel
description: ""
seo:
 title: ""
 description: ""
---

If you only need to run a single OpenFAST simulation, then you should run it on your desktop machine: it will be faster there due to the much higher 
clock speeds. However, if you need to run hundreds or thousands of OpenFAST simulations, you can use the Inductiva API to spin up hundreds of very cheap cloud machines 
to run all these simulations in parallel, instead of running them sequentially on your machine! This is hundreds of times faster. And it is super easy 
(and cost-effective) to do with Inductiva.

In this tutorial, we are going to show you how you can
use the Inductiva API to accelerate your OpenFAST projects, by showing how to
run dozens of simulations in parallel.

:raw-img{src="/openfast/openfast_animation_30_fps.gif" alt="OpenFAST simulation visualization" center}

To demonstrate this, we will use the [`5MW_OC4Semi_WSt_WavesWN`](https://github.com/OpenFAST/r-test/tree/v4.0.2/glue-codes/openfast/5MW_OC4Semi_WSt_WavesWN) example, available on the [OpenFAST GitHub repository](https://github.com/openfast).

This example is an extension of the reference case described in ["Definition of a 5-MW Reference Wind Turbine for Offshore
System Development"](https://www.nrel.gov/docs/fy09osti/38060.pdf).

The tutorial is divided into the following sections:
- [Set up the example files](/guides/openfast/tutorials/run-50-simulations-in-parallel/section1)
- [Run a single simulation using the Inductiva API](/guides/openfast/tutorials/run-50-simulations-in-parallel/section2)
- [Generalize the use case](/guides/openfast/tutorials/run-50-simulations-in-parallel/section3)
- [Launch and manage 50 simulations in parallel on the cloud](/guides/openfast/tutorials/run-50-simulations-in-parallel/section4)
- [Post-process and analyze simulation results](/guides/openfast/tutorials/run-50-simulations-in-parallel/section5)

::docsbannersmall
::
