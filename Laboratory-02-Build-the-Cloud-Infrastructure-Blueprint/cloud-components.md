# Cloud Infrastructure Components

## Overview

Cloud infrastructure is composed of different resources that work together to provide computing services. The major components include compute resources, storage resources, networking resources, and the operating system. These components can be observed and investigated in the Linux environment provided by KillerCoda.

---

## 1. Compute Resources

### Purpose

Compute resources provide the processing power needed to run applications, process data, and perform computing tasks. These resources mainly include the CPU and processor cores.

### Importance in Cloud Computing

Compute resources are important because cloud applications and services need processing power to operate. Cloud providers can provide different amounts of computing resources depending on the requirements of users and applications.

### Relation to the KillerCoda Linux Environment

In the KillerCoda Linux environment, the CPU model and the number of CPU cores are examples of compute resources. These can be investigated using the `lscpu` and `nproc` commands.

---

## 2. Storage Resources

### Purpose

Storage resources are used to store the operating system, applications, files, and other important data.

### Importance in Cloud Computing

Storage is important because cloud applications need a reliable location to save and access data. Cloud storage allows users and applications to store information and retrieve it when needed.

### Relation to the KillerCoda Linux Environment

In the KillerCoda Linux environment, disk capacity and mounted file systems are examples of storage resources. These can be investigated using commands such as `lsblk` and `df -h`.

---

## 3. Networking Resources

### Purpose

Networking resources allow computers, servers, applications, and users to communicate with each other through a network.

### Importance in Cloud Computing

Networking is important because cloud services depend on network and internet connections. It allows users to access cloud applications and enables communication between different cloud resources.

### Relation to the KillerCoda Linux Environment

In the KillerCoda Linux environment, the IP address and network interfaces are examples of networking resources. These can be investigated using the `ip addr` command.

---

## 4. Operating System

### Purpose

The operating system manages the hardware and software resources of a computer or server. It provides the environment needed to run applications and services.

### Importance in Cloud Computing

An operating system is important because it manages processes, memory, storage, networking, and applications running on a cloud server. Linux is commonly used in cloud environments because it provides a stable and flexible environment for managing servers.

### Relation to the KillerCoda Linux Environment

The KillerCoda environment runs a Linux operating system. Information about the operating system can be investigated using the `cat /etc/os-release` command, while the kernel version can be checked using `uname -r`.

---

## Conclusion

Compute, storage, networking, and operating systems are important components of cloud infrastructure. These components work together to provide the resources needed to run applications and services in a cloud environment. Investigating these resources in KillerCoda helped demonstrate how a Linux server provides the foundation for cloud computing.
