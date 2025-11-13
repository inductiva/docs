---
title: Launching Machines on Your Own GCP Account
description: ""
navigation:
  show: false
seo:
 title: “”
 description: “”
---

Inductiva's Bring Your Own Cloud (BYOC) feature allows you to launch and manage compute machines directly on your own Google Cloud Platform (GCP) account. This gives you full control over your compute resources while leveraging Inductiva's task management and simulation capabilities. Your GCP credentials never leave your local machine, ensuring maximum security and privacy.

BYOC enables you to:
- **Reduce costs** by using your own GCP credits and billing account
- **Maintain control** over your compute infrastructure and security policies
- **Scale seamlessly** while keeping compute resources within your organization
- **Comply** with organizational policies that require compute to remain in your cloud account
- **Run simulations seamlessly** with the same experience as Inductiva's managed infrastructure


## Prerequisites

Before you begin, ensure you have:

- **A Google Cloud Platform (GCP) account** with a valid billing account attached
- **Inductiva Python client** installed: See the [Installation Guide](/guides/get-started/install-guide) for detailed instructions.

## Get Started

**[How It Works](/guides/bring-your-own-cloud/launch-machines-on-gcp/sections/section1):** Detailed explanation of the BYOC architecture and security model.

**[Installation and Setup](/guides/bring-your-own-cloud/launch-machines-on-gcp/sections/section2):** Installation steps, permissions, GCP CLI configuration, testing, and disclaimers.

**[Python Client Usage](/guides/bring-your-own-cloud/launch-machines-on-gcp/sections/section3):** Create and manage BYOC machine groups using the Inductiva Python client.

**[Command Line Usage](/guides/bring-your-own-cloud/launch-machines-on-gcp/sections/section4):** Launch and manage BYOC machine groups using the Inductiva CLI.

**[Frequently Asked Questions](/guides/bring-your-own-cloud/launch-machines-on-gcp/sections/section5):** Comprehensive FAQ covering setup, usage, troubleshooting, limitations, and common questions about BYOC on GCP.

## Disclaimer

When using BYOC, you are responsible for:
- **All costs** incurred by VMs running in your GCP account
- **Managing and monitoring** your compute resources
- **Ensuring compliance** with your organization's policies
- **Properly terminating** machines to avoid unexpected charges

**Note:** Inductiva provides auto-termination (default: 3 minutes of idle time) as a best-effort safety feature to help prevent forgotten VMs.

**Inductiva is not responsible for:**
- Unexpected charges from VMs left running in your account
- Data loss or security incidents on your GCP infrastructure
- Compliance issues with your organization's policies
- Any damage to your GCP resources or data

**Recommendation:** Always monitor your GCP console and set up billing alerts to track usage and costs.

::docsbanner
::

