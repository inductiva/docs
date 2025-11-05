---
title: Architecture Overview
description: ""
navigation:
    show: true
    title: Overview
seo:
 title: “”
 description: “”
---

The Inductiva API centrally manages all your cloud resources, simulation tasks, and storage. The Python Client, CLI, and Web Console are the different interfaces you can use to communicate with these resources.

The following diagram illustrates this relationship:

![Building Blocks](how-it-works/building_blocks.png)

1. Start and manage remote Virtual Machines (VMs), operating either independently
or collectively, that are equipped with pre-installed simulation software.

2. Send your simulation scripts from your laptop to one or more remote machines,
and start the simulators.

3. Download simulation results, selecting either all data files generated or
specific ones of interest.

That’s it! While this outlines the basic flow of usage of the API, there are
nuances and additional options available, which we'll explore in detail throughout
this section. More specifically, you'll become familiarized with how the API
works:

- [Tasks](/guides/tasks/):
Learn about tasks, the API's core computational object, which
gets created when you submit your simulation request, enabling you to track its
progress and access its outputs in real-time.

- [Computational Resources](/guides/machines/):
Discover how the API allocates and runs your simulation tasks on **dedicated** 
computational resources. Take a further look under the hood to learn the underlying 
infrastructure powering your simulations, especially how the API enables you to access 
a variety of computational resources, manages your computational workload, and allocates 
it to the appropriate computational resource through a unified Python code.

- [Built-in Simulators](/guides/building-blocks/configuring-simulators):
Explore how the API wraps existing open-source software packages within layers that 
facilitate their execution across various cloud-based virtual machines and providers, 
transforming them into abstract computational tasks.

- [Storage and Data Flow](/guides/cloud-storage/cloud-storage):
Get to know the typical flow of data when you invoke a remote simulator using the 
Inductiva API, from sending your input files to remote computational resources to 
accessing the simulation outputs.

::docsbanner
::
