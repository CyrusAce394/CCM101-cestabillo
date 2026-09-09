# Laboratory 03: Become a Multi-Cloud Explorer

## Overview
This laboratory activity explores the core offerings, global infrastructure, and target use cases of Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP). It includes service comparison matrices, business case recommendations, service equivalent mapping, and a cloud migration plan for a Linux environment.

---

# Checkpoint 7: Linux Server Investigation

### Terminal Commands Executed on KillerCoda
The following commands were run inside the KillerCoda terminal environment to determine the system's specs:

```bash
# Identify Operating System details
cat /etc/os-release

# Inspect CPU architecture and specifications
lscpu

# Check total and available system memory
free -h

# Check available disk storage and partition sizes
df -h
```

### Terminal Command Outputs

#### 1. Operating System Details (`cat /etc/os-release`)
```plaintext
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
```

#### 2. CPU Information (`lscpu`)
```plaintext
Architecture:                x86_64
  CPU op-mode(s):            32-bit, 64-bit
  Address sizes:             39 bits physical, 48 bits virtual
  Byte Order:                Little Endian
CPU(s):                      1
  On-line CPU(s) list:       0
Vendor ID:                   GenuineIntel
  BIOS Vendor ID:            Red Hat
  Model name:                Intel Xeon E312xx (Sandy Bridge, IBRS update)
    BIOS Model name:         RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz
    BIOS CPU family:         1
    CPU family:              6
    Model:                   42
    Thread(s) per core:      1
    Core(s) per socket:      1
    Socket(s):               1
    Stepping:                1
    BogoMIPS:                7008.00
Virtualization features:     
  Hypervisor vendor:         KVM
  Virtualization type:       full
```

#### 3. Memory Information (`free -h`)
```plaintext
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       410Mi       869Mi       1.1Mi       790Mi       1.5Gi
Swap:          1.0Gi          0B       1.0Gi
```

#### 4. Disk Space Information (`df -h`)
```plaintext
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  996K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K  952M   1% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   6% /boot/efi
```

---

### System Summary
* **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
* **CPU:** 1 vCPU (Intel Xeon E312xx @ 2.0GHz, x86_64 architecture)
* **Memory:** 1.9 GiB RAM (~2.0 GB)
* **Disk Space:** 19 GB Root Disk (`/dev/vda1`)

---

### Cloud Migration Analysis
If this on-premises or virtual Linux server were migrated to a public cloud provider, the equivalent virtual machine hosting options across AWS, Azure, and GCP based on its exact specs (1 vCPU, 2 GiB RAM, ~20 GB Disk) are:

#### 1. Amazon Web Services (AWS)
* **Compute Service:** Amazon EC2 (Elastic Compute Cloud)
* **Instance Type:** `t3.small` or `t4g.small` (1 vCPU, 2 GiB RAM)
* **Storage:** Amazon EBS (Elastic Block Store) - 20 GB General Purpose SSD (`gp3`)

#### 2. Microsoft Azure
* **Compute Service:** Azure Virtual Machines
* **VM Size:** `Standard_B1ms` (1 vCPU, 2 GiB RAM)
* **Storage:** Azure Premium SSD Managed Disk (32 GB)

#### 3. Google Cloud Platform (GCP)
* **Compute Service:** Google Compute Engine (GCE)
* **Machine Type:** `e2-micro` or `e2-small` (1–2 vCPUs, 2 GiB RAM)
* **Storage:** GCP Standard Persistent Disk (20 GB)
