
# System Baseline Report

## Laboratory 07 – Cloud Operations Engineer

### Checkpoint 2: Establish a Host System Baseline

## 1. Memory (RAM) Check

**Command Executed:**

```bash
free -h
```

**Terminal Output:**

```text
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       422Mi       1.1Gi       1.1Mi       500Mi       1.4Gi
Swap:          1.0Gi          0B       1.0Gi
```

**Total RAM on the Server:** 1.9 GiB

**Currently Available RAM:** 1.4 GiB

The server has a total memory capacity of 1.9 GiB, with 1.4 GiB currently available for running applications and processes.

---

## 2. Disk Storage Check

**Command Executed:**

```bash
df -h /
```

**Terminal Output:**

```text
Filesystem      Size  Used Avail Use% Mounted on
/dev/vda1        19G  5.5G   13G  30% /
```

**Total Storage Capacity of the Root (/) File System:** 19 GB

**Used Storage:** 5.5 GB

**Available Storage:** 13 GB

**Disk Usage:** 30%

The root file system has a total storage capacity of 19 GB, with 13 GB available and 30% of the storage currently used.

---

## 3. CPU and Process Monitoring

**Command Executed:**

```bash
top
```

**Terminal Output:**

```text
top - 23:41:31 up  3:42,  0 user,  load average: 0.00, 0.00, 0.00
Tasks: 131 total,   1 running, 130 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.3 ni, 99.7 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   1903.2 total,   1126.7 free,    430.7 used,    517.5 buff/cache
MiB Swap:   1024.0 total,   1024.0 free,      0.0 used.   1472.6 avail Mem
```

### CPU and Process Analysis

- **CPU Idle:** 99.7%
- **CPU Nice Usage:** 0.3%
- **Load Average:** 0.00, 0.00, 0.00
- **Total Tasks:** 131
- **Running Tasks:** 1
- **Sleeping Tasks:** 130
- **Stopped Tasks:** 0
- **Zombie Tasks:** 0
- **Total Memory:** 1903.2 MiB
- **Free Memory:** 1126.7 MiB
- **Used Memory:** 430.7 MiB
- **Buffer/Cache:** 517.5 MiB
- **Available Memory:** 1472.6 MiB
- **Total Swap Memory:** 1024.0 MiB
- **Used Swap Memory:** 0.0 MiB

---

## 4. Importance of Checking Disk Space

Checking disk space before a massive traffic surge is important because increased website traffic can generate additional logs and temporary files that may fill the server's storage and cause application errors or downtime.
