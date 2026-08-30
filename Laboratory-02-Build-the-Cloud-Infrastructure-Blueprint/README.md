
# Laboratory 02: Build the Cloud Infrastructure Blueprint

## Mission Overview
This laboratory activity simulates the initial planning and assessment phase of a cloud migration for an enterprise client[cite: 1]. As part of CloudNova Technologies, the goal is to investigate a cloud-hosted Linux server, identify core infrastructure primitives, evaluate service offerings across major cloud providers, and prepare technical documentation before system deployment[cite: 1].

---

## Objectives
* Investigate the hardware and software resources available in a cloud Linux environment[cite: 1].
* Identify and explain the core components of cloud infrastructure (Compute, Storage, Networking, OS)[cite: 1].
* Compare equivalent core cloud services across AWS, Microsoft Azure, and GCP[cite: 1].
* Design a simple cloud infrastructure architecture diagram[cite: 1].
* Maintain a professional GitHub portfolio with proper Markdown technical documentation[cite: 1].

---

## Cloud Infrastructure Components
* **Compute:** CPU cores and RAM allocated for executing application workloads and processing data[cite: 1].
* **Storage:** Persistent block and object storage for operating system files, user data, and backups[cite: 1].
* **Networking:** Virtual networks, subnets, and IP addresses enabling system and internet communication[cite: 1].
* **Operating System:** Linux OS serving as the foundation for software execution and server operations[cite: 1].

---

## Tools Used
* **KillerCoda Playground:** Cloud-hosted Linux terminal environment[cite: 1].
* **GitHub:** Version control and technical portfolio repository[cite: 1].
* **Excalidraw / Draw.io:** Cloud architecture diagramming tool[cite: 1].
* **VS Code / Web Markdown Editor:** Technical documentation drafting[cite: 1].

---

## Linux Commands Executed

| Command | Description / Purpose |
| :--- | :--- |
| `uname -a` / `cat /etc/os-release` | Inspected operating system details, version, and kernel details[cite: 1]. |
| `lscpu` | Extracted CPU architecture, model name, and total CPU cores[cite: 1]. |
| `free -h` | Displayed total, used, and available system RAM (Memory)[cite: 1]. |
| `df -h` | Examined disk capacity, partition usage, and filesystem mounts[cite: 1]. |
| `hostname` & `ip a` | Identified the server's network hostname and active IP addresses[cite: 1]. |

---

## Cloud Architecture Diagram

Below is the simple cloud infrastructure blueprint designed for this mission[cite: 1]:

![Cloud Architecture Blueprint](./screenshots/cloud-architecture.png)[cite: 1]

---

## Skills Learned & Challenges Encountered

### Skills Learned
* Auditing physical/virtual hardware resources using fundamental Linux CLI commands[cite: 1].
* Cross-referencing service equivalents among AWS, Azure, and Google Cloud Platform[cite: 1].
* Constructing cloud architecture blueprints visually[cite: 1].
* Structuring clean, professional Markdown files for engineering documentation[cite: 1].

### Challenges Encountered
* **Challenge:** Remembering specific flags for Linux system inspection commands (e.g., `-h` for human-readable output in `df` and `free`)[cite: 1].
* **Resolution:** Referred to command `man` pages and help flags to format outputs effectively[cite: 1].
