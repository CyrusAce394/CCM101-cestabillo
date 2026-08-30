# Laboratory 02: Build the Cloud Infrastructure Blueprint

## Mission Overview
This laboratory activity simulates the initial planning and assessment phase of a cloud migration for an enterprise client. As part of CloudNova Technologies, the goal is to investigate a cloud-hosted Linux server, identify core infrastructure primitives, evaluate service offerings across major cloud providers, and prepare technical documentation before system deployment.

---

## Objectives
* Investigate the hardware and software resources available in a cloud Linux environment.
* Identify and explain the core components of cloud infrastructure (Compute, Storage, Networking, OS).
* Compare equivalent core cloud services across AWS, Microsoft Azure, and GCP.
* Design a simple cloud infrastructure architecture diagram.
* Maintain a professional GitHub portfolio with proper Markdown technical documentation.

---

## Cloud Infrastructure Components
* **Compute:** CPU cores and RAM allocated for executing application workloads and processing data.
* **Storage:** Persistent block and object storage for operating system files, user data, and backups.
* **Networking:** Virtual networks, subnets, and IP addresses enabling system and internet communication.
* **Operating System:** Linux OS serving as the foundation for software execution and server operations.

---

## Tools Used
* **KillerCoda Playground:** Cloud-hosted Linux terminal environment.
* **GitHub:** Version control and technical portfolio repository.
* **Eraser.io:** Cloud architecture diagramming tool.

---

## Linux Commands Executed

| Command | Description / Purpose |
| :--- | :--- |
| `uname -a` / `cat /etc/os-release` | Inspected operating system details, version, and kernel details. |
| `lscpu` | Extracted CPU architecture, model name, and total CPU cores. |
| `free -h` | Displayed total, used, and available system RAM (Memory). |
| `df -h` | Examined disk capacity, partition usage, and filesystem mounts. |
| `hostname` & `ip a` | Identified the server's network hostname and active IP addresses. |

---

## Cloud Architecture Diagram

Below is the simple cloud infrastructure blueprint designed for this mission:

![Cloud Architecture Blueprint](./screenshots/checkpoint5/cloud-architecture.png)

---

## Skills Learned & Challenges Encountered

### Skills Learned
* Auditing physical/virtual hardware resources using fundamental Linux CLI commands.
* Cross-referencing service equivalents among AWS, Azure, and Google Cloud Platform.
* Constructing cloud architecture blueprints visually.
* Structuring clean, professional Markdown files for engineering documentation.

### Challenges Encountered
* **Challenge:** Remembering specific flags for Linux system inspection commands (e.g., `-h` for human-readable output in `df` and `free`).
* **Resolution:** Referred to command `man` pages and help flags to format outputs effectively.
