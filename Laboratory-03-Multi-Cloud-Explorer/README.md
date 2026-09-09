# Laboratory 03: Become a Multi-Cloud Explorer

## Overview
This laboratory activity explores the core offerings, global infrastructure, and target use cases of Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP). It includes service comparison matrices, business case recommendations, service equivalent mapping, and a cloud migration plan for a Linux environment.

---

## File Index
* [`aws-research.md`](./aws-research.md) – Overview, global infrastructure, core services, advantages, and enterprise use cases for AWS.
* [`azure-research.md`](./azure-research.md) – Overview, global infrastructure, core services, advantages, and enterprise use cases for Microsoft Azure.
* [`gcp-research.md`](./gcp-research.md) – Overview, global infrastructure, core services, advantages, and enterprise use cases for Google Cloud Platform.
* [`cloud-platform-comparison.md`](./cloud-platform-comparison.md) – Detailed comparison table, direct analysis answers, and cloud service equivalent reference table.
* [`client-recommendations.md`](./client-recommendations.md) – Scenario-based cloud platform recommendations and multi-cloud decision matrix.
* [`reflection.md`](./reflection.md) – Reflection on multi-cloud architectures and practical takeaways.

---

## Checkpoint 7: Linux Server Investigation

### Terminal Commands Executed on KillerCoda
The following Linux commands were executed inside the KillerCoda playground environment to gather host system hardware and operating system specifications:

```bash
# Identify Operating System details
cat /etc/os-release

# Inspect CPU architecture and specifications
lscpu

# Check total and available system memory
free -h

# Check available disk storage and partition sizes
df -h
