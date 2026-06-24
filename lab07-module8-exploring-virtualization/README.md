# Lab 07 – Exploring Virtualization with Ubuntu Server VM

## Objective

The objective of this lab was to explore virtualization concepts by creating, configuring, and documenting an Ubuntu Server virtual machine running inside UTM on macOS.

This lab demonstrates key virtualization concepts including hypervisors, virtual machines, resource allocation, virtual storage, virtual networking, guest operating systems, recovery points, and Linux system verification.

---

## Lab Environment

| Component              | Details                   |
| ---------------------- | ------------------------- |
| Host System            | macOS                     |
| Hypervisor             | UTM                       |
| Virtualization Engine  | QEMU                      |
| Guest Operating System | Ubuntu Server 24.04.4 LTS |
| Architecture           | ARM64 / aarch64           |
| VM Memory              | 4 GB                      |
| Virtual CPUs           | 4 cores                   |
| Network Mode           | Shared Network            |
| Virtual Disk           | VirtIO Disk Image         |

---

## Screenshots

### 1. Hypervisor Overview

This screenshot shows the Ubuntu virtual machine listed inside UTM. It documents the hypervisor interface, VM status, architecture, memory, storage, and network mode.

---

### 2. VM Settings

The VM settings show the system configuration, including ARM64 architecture, QEMU machine type, allocated memory, and CPU configuration.

---

### 3. CPU Allocation

The virtual machine was configured with 4 virtual CPU cores.

---

### 4. Memory Allocation

The VM was allocated 4096 MiB of memory, which is approximately 4 GB of RAM.

---

### 5. Virtual Storage

The VM uses a VirtIO virtual disk image in qcow2 format.

---

### 6. Virtual Networking

The VM was configured with Shared Network mode using the virtio-net-pci virtual network card.

---

### 7. Ubuntu Server Boot

Ubuntu Server successfully booted into the command-line interface. Although this VM does not use a graphical desktop environment, the terminal interface is ideal for server administration, networking, Linux administration, and cybersecurity labs.

---

### 8. System Information

The `hostnamectl` command was used to verify system details.

Command used:

```bash
hostnamectl
```

Key results:

| Field            | Value                   |
| ---------------- | ----------------------- |
| Hostname         | ubuntu-lab              |
| Operating System | Ubuntu 24.04.4 LTS      |
| Kernel           | Linux 6.8.0-106-generic |
| Architecture     | arm64                   |
| Virtualization   | qemu                    |

---

### 9. CPU Information

The `lscpu` command was used to verify CPU architecture and virtual CPU allocation.

Command used:

```bash
lscpu
```

Key results:

| Field            | Value   |
| ---------------- | ------- |
| Architecture     | aarch64 |
| CPU Mode         | 64-bit  |
| CPUs             | 4       |
| Vendor ID        | Apple   |
| Cores per Socket | 4       |

---

### 10. Memory Usage

The `free -h` command was used to verify memory usage.

Command used:

```bash
free -h
```

Key results:

| Metric        | Value   |
| ------------- | ------- |
| Total RAM     | 3.8 GiB |
| Used RAM      | 287 MiB |
| Free RAM      | 3.5 GiB |
| Available RAM | 3.5 GiB |
| Swap          | 3.8 GiB |

---

### 11. Disk Usage

The `df -h` command was used to verify disk usage.

Command used:

```bash
df -h
```

Key results:

| Filesystem | Size | Used | Available | Usage |
| ---------- | ---: | ---: | --------: | ----: |
| /dev/vda2  |  39G | 6.7G |       30G |   19% |
| /dev/vda1  | 1.1G | 6.4M |      1.1G |    1% |

---

### 12. Network Configuration

The `ip a` command was used to identify the network interface and IP address.

Command used:

```bash
ip a
```

Key results:

| Item         | Value              |
| ------------ | ------------------ |
| Interface    | enp0s1             |
| State        | UP                 |
| IPv4 Address | 192.168.64.2/24    |
| MAC Address  | Hidden for privacy |

---

### 13. Internet Connectivity Test

The `ping` command was used to verify DNS resolution and Internet connectivity.

Command used:

```bash
ping -c 4 google.com
```

Results:

| Test             | Result              |
| ---------------- | ------------------- |
| DNS Resolution   | Successful          |
| Packets Sent     | 4                   |
| Packets Received | 4                   |
| Packet Loss      | 0%                  |
| Average Latency  | Approximately 38 ms |

---

### Recovery Point

UTM did not provide a traditional snapshot option in this VM configuration. Instead, the virtual machine was duplicated and saved as a baseline recovery point.

This duplicate VM can be used to restore a clean environment before performing future labs or major system changes.

---

## Key Virtualization Concepts Demonstrated

| Concept                | Demonstrated By                  |
| ---------------------- | -------------------------------- |
| Hypervisor             | UTM                              |
| Virtual Machine        | Ubuntu Server                    |
| Guest Operating System | Ubuntu Server 24.04.4 LTS        |
| CPU Allocation         | 4 Virtual CPUs                   |
| Memory Allocation      | 4096 MiB                         |
| Virtual Storage        | qcow2 VirtIO Disk                |
| Virtual Networking     | Shared Network                   |
| Linux Administration   | hostnamectl, lscpu, free, df, ip |
| Internet Connectivity  | ping                             |
| Recovery Planning      | VM Duplication                   |

---

## Lessons Learned

This lab helped me understand how virtualization allows a complete operating system to run inside another physical computer. I learned how to review VM hardware settings, verify resources from inside the guest operating system, check network configuration, and confirm Internet connectivity.

I also learned that Ubuntu Server does not include a graphical desktop environment by default. Instead, it uses a command-line interface, which is widely used in Linux administration, networking, cloud environments, and cybersecurity.

Finally, I learned the importance of creating a recovery point before making system changes. Since UTM did not provide a traditional snapshot option for this VM, duplicating the VM created an effective baseline backup.

---

## Skills Practiced

* Virtual machine management
* Hypervisor navigation
* Linux command-line administration
* CPU and memory verification
* Disk usage analysis
* Network interface inspection
* Connectivity testing
* Recovery planning
* Technical documentation

---

## Conclusion

This lab provided hands-on experience with virtualization using UTM and Ubuntu Server. The VM was configured with virtual CPU, memory, storage, and networking resources, then verified from inside the Linux guest operating system.

This project supports my learning path toward CompTIA A+, Network+, and cybersecurity by building practical experience with Linux, virtual machines, networking, and system administration.
