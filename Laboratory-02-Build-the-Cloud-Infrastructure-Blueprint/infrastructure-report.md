# Cloud Infrastructure Report

## Laboratory Activity 2: Build the Cloud Infrastructure Blueprint

This report presents the results of the investigation of the Linux cloud server environment using KillerCoda.

---

## 1. Operating System

**Command Used:**

```bash
cat /etc/os-release
```

**Result:**
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


---

## 2. Kernel Version

**Command Used:**

```bash
uname -r
```

**Result:**

[6.8.0-138-generic]

---

## 3. CPU Model

**Command Used:**

```bash
lscpu
```

**Result:**

[Architecture:                x86_64
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
    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscal
                             l nx rdtscp lm constant_tsc rep_good nopl xtopology cpuid tsc_known_freq pni pclmulqdq ssse3 cx16 pcid s
                             se4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs
                              ibpb stibp tsc_adjust xsaveopt arat md_clear
Virtualization features:     
  Hypervisor vendor:         KVM
  Virtualization type:       full
Caches (sum of all):         
  L1d:                       32 KiB (1 instance)
  L1i:                       32 KiB (1 instance)
  L2:                        4 MiB (1 instance)
  L3:                        16 MiB (1 instance)
NUMA:                        
  NUMA node(s):              1
  NUMA node0 CPU(s):         0
Vulnerabilities:             
  Gather data sampling:      Not affected
  Indirect target selection: Mitigation; Aligned branch/return thunks
  Itlb multihit:             KVM: Mitigation: VMX unsupported
  L1tf:                      Mitigation; PTE Inversion
  Mds:                       Mitigation; Clear CPU buffers; SMT Host state unknown
  Meltdown:                  Mitigation; PTI
  Mmio stale data:           Unknown: No mitigations
  Reg file data sampling:    Not affected
  Retbleed:                  Not affected
  Spec rstack overflow:      Not affected
  Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected
                             ; BHI Retpoline
  Srbds:                     Not affected
  Tsa:                       Not affected
  Tsx async abort:           Not affected
  Vmscape:                   Not affected]

---

## 4. Number of CPU Cores

**Command Used:**

```bash
nproc
```

**Result:**

[1]

---

## 5. Total RAM

**Command Used:**

```bash
free -h
```

**Result:**

[               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       415Mi       866Mi       1.1Mi       789Mi       1.5Gi
Swap:          1.0Gi          0B       1.0Gi]

---

## 6. Disk Capacity

**Command Used:**

```bash
lsblk
```

**Result:**

[NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINTS
vda     253:0    0   20G  0 disk 
|-vda1  253:1    0   19G  0 part /
|-vda14 253:14   0    4M  0 part 
|-vda15 253:15   0  106M  0 part /boot/efi
`-vda16 259:0    0  913M  0 part /boot]

---

## 7. Mounted File Systems

**Command Used:**

```bash
df -h
```

**Result:**

[Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  996K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K  952M   1% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   6% /boot/efi]

---

## 8. Hostname

**Command Used:**

```bash
hostname
```

**Result:**

[ubuntu]

---

## 9. IP Address

**Command Used:**

```bash
ip addr
```

**Result:**

[1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: enp1s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1450 qdisc fq_codel state UP group default qlen 1000
    link/ether fe:d4:44:d5:e6:4a brd ff:ff:ff:ff:ff:ff
    inet 172.30.1.2/24 brd 172.30.1.255 scope global dynamic noprefixroute enp1s0
       valid_lft 86311816sec preferred_lft 75522616sec
    inet6 fe80::699c:b250:a2a:c039/64 scope link 
       valid_lft forever preferred_lft forever
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1454 qdisc noqueue state DOWN group default 
    link/ether 32:20:b2:e5:77:b5 brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever]

---

# Summary

The KillerCoda Linux environment was investigated to identify its operating system, kernel version, CPU resources, memory, storage, networking information, and hostname. These components are important in cloud computing because they provide the compute, storage, networking, and system resources needed to run cloud-based applications and services.
