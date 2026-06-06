# Module 3 Lab – Computer Hardware and Architecture Analysis

## Objective

Analyze the hardware components and architecture of a MacBook Air using macOS system tools, Activity Monitor, Disk Utility, and Terminal commands.

---

# Device Specifications

| Component | Details |
|------------|----------|
| Model | MacBook Air (2022) |
| Processor | Apple M2 |
| Memory | 8 GB Unified Memory |
| Storage | 256 GB SSD (245.11 GB usable) |
| Operating System | macOS Tahoe 26.5 |
| Display | 13.6-inch Liquid Retina Display (2560 × 1664) |

---

# Hardware Analysis

## Processor

The MacBook Air is equipped with an Apple M2 System-on-Chip (SoC) featuring:

- 8 CPU cores
  - 4 Performance cores
  - 4 Efficiency cores
- Integrated GPU
- Neural Engine
- Unified Memory Architecture

This hybrid design balances performance and power efficiency by assigning demanding tasks to performance cores while background processes run on efficiency cores.

---

## Memory

The system contains:

- 8 GB LPDDR5 Unified Memory

Unlike traditional PCs, Apple Silicon uses Unified Memory Architecture (UMA), allowing the CPU, GPU, and Neural Engine to access the same memory pool.

### Advantages

- Faster communication between components
- Reduced memory duplication
- Improved power efficiency
- Better battery life

### Disadvantages

- Memory cannot be upgraded after purchase
- RAM is soldered to the system

---

## Storage Analysis

The MacBook Air uses a solid-state drive (SSD) with a capacity of 245.11 GB.

Storage observations:

- SSD technology provides significantly faster performance than traditional HDDs.
- APFS supports snapshots, encryption, and efficient space allocation.
- Full-disk encryption is enabled.
- The storage device is integrated into the Apple Silicon platform.
- Approximately 66.97 GB of free space was available during analysis.

The drive is configured as an APFS Volume Group containing separate system and data volumes.

---

## Apple File System (APFS)

APFS (Apple File System) is Apple's modern file system optimized for SSD storage.

### Key Features

- Native encryption
- Snapshot support
- Space sharing between volumes
- Improved reliability
- Optimized flash storage performance

APFS replaces the older HFS+ file system previously used on macOS devices.

---

## SSD Advantages

Compared to traditional hard disk drives (HDDs), SSDs provide:

- Faster boot times
- Faster application loading
- Lower power consumption
- No moving parts
- Improved durability
- Reduced heat generation

---

# Performance Analysis

## CPU Utilization

Activity Monitor showed the Apple M2 processor operating under a very light workload.

### Results

- System CPU Usage: 1.41%
- User CPU Usage: 2.59%
- Idle CPU: 96%
- Processes Running: 474
- Threads: 2,508

Despite multiple applications and browser tabs being open, CPU utilization remained extremely low, demonstrating the efficiency of Apple Silicon architecture.

---

## Memory Utilization

The system contains 8 GB of Unified LPDDR5 memory.

### Observations

During testing:

- Memory Used: ~7 GB
- Cached Files: ~1 GB
- Swap Usage: 1.4–1.8 GB

The operating system used memory compression and swap storage to efficiently manage active workloads.

### Memory Management

The `vm_stat` command showed evidence of:

- Memory compression
- Virtual memory usage
- Swap activity

These mechanisms allow macOS to continue operating efficiently when physical memory becomes limited.

---

# Apple Silicon Architecture

The Apple M2 processor is based on ARM architecture, which follows the Reduced Instruction Set Computing (RISC) design philosophy.

### Advantages

- Lower power consumption
- Improved battery life
- Reduced heat generation
- High performance per watt

### Hybrid Core Design

The M2 processor uses:

- Performance cores for demanding workloads
- Efficiency cores for background tasks

This design improves overall performance while maintaining excellent energy efficiency.

---

# Terminal Hardware Analysis

The following Terminal commands were used to gather hardware and operating system information.

## Hardware Information

Command:

```bash
system_profiler SPHardwareDataType
```

Results confirmed:

- MacBook Air (Mac14,2)
- Apple M2 processor
- 8 CPU cores
- 8 GB memory

Terminal-based hardware inventory provides an efficient method for gathering system information during troubleshooting and audits.

---

## Memory Statistics

Command:

```bash
vm_stat
```

This command displayed:

- Active memory pages
- Inactive memory pages
- Compressed memory pages
- Swap activity
- Page-ins and page-outs

The results supported observations from Activity Monitor regarding virtual memory and memory compression.

---

## Disk Layout Analysis

Command:

```bash
diskutil list
```

This command revealed the APFS container structure used by macOS.

Observed volumes included:

- Macintosh HD
- Data
- Recovery
- Preboot
- VM

This structure separates operating system files from user data and recovery resources, improving system reliability and recovery capabilities.

---

# ARM Architecture Verification

Command:

```bash
uname -m
```

Result:

```text
arm64
```

This confirms that the MacBook Air uses:

- ARM architecture
- Apple Silicon
- 64-bit instruction set

---

# ARM vs x86 Comparison

| Feature | ARM | x86 |
|----------|------|------|
| Power Consumption | Lower | Higher |
| Battery Life | Better | Lower |
| Heat Generation | Lower | Higher |
| Performance per Watt | Excellent | Moderate |
| Legacy Software Support | Limited | Extensive |
| Upgradeability | Limited | Greater |

Apple's transition to ARM-based Apple Silicon processors has significantly improved performance and energy efficiency in modern Mac systems.

---

# RAID Comparison

| RAID Level | Description | Advantages | Disadvantages |
|------------|-------------|-------------|---------------|
| RAID 0 | Striping | High performance | No fault tolerance |
| RAID 1 | Mirroring | Redundancy | 50% storage efficiency |
| RAID 5 | Striping with parity | Balance of speed and protection | Requires 3+ drives |
| RAID 10 | Mirroring and striping | High performance and redundancy | Higher hardware cost |

Although the MacBook Air does not use RAID, understanding RAID technologies is important for enterprise storage environments.

---

# Upgradeability Assessment

The MacBook Air M2 has limited upgradeability because major components are integrated into the Apple Silicon platform.

## Limitations

- Soldered memory
- Integrated SSD storage
- Non-user-serviceable internal components

## Advantages

- Smaller form factor
- Improved power efficiency
- Better thermal performance

## Disadvantages

- Limited hardware upgrades
- Higher repair complexity
- Reduced component replacement options

---

# Screenshots

## Figure 1 – About This Mac Overview

Shows the MacBook Air hardware specifications including the Apple M2 chip, installed memory, and operating system version.

---

## Figure 2 – Storage Overview

Displays storage utilization and available disk space on the internal SSD.

---

## Figure 3 – Hardware Overview

Displays detailed hardware specifications including the Apple M2 chip, CPU core configuration, and system memory.

---

## Figure 4 – Storage Information

Shows APFS volumes, SSD details, storage capacity, and storage health status.

---

## Figure 5 – Memory Information

Displays installed LPDDR5 memory used by the Apple Silicon unified memory architecture.

---

## Figure 6 – CPU Performance

Displays CPU utilization, process count, and thread count while the system is running multiple applications.

---

## Figure 7 – Memory Usage

Displays memory pressure, memory utilization, cached files, and swap memory usage.

---

## Figure 8 – Memory Usage Under Additional Load

Shows increased memory consumption after opening additional browser tabs and applications.

---

## Figure 9 – Disk Utility Overview

Displays the APFS volume group, available storage capacity, and current disk utilization.

---

## Figure 10 – Disk Information

Shows detailed file system information, encryption status, volume configuration, and storage characteristics.

---

## Figure 11 – Terminal Hardware Profile

Displays hardware inventory information gathered through Terminal.

---

## Figure 12 – Terminal Memory Statistics

Shows memory management statistics including paging and compression activity.

---

## Figure 13 – Terminal Disk Layout

Displays the APFS container structure and storage configuration.

---

## Figure 14 – ARM Architecture Verification

Confirms the system is running on ARM64 architecture.

---

# Conclusion

This lab examined the hardware architecture of a MacBook Air equipped with Apple's M2 processor.

Using macOS system tools and Terminal commands, hardware specifications, memory utilization, storage configuration, and processor architecture were analyzed.

The system demonstrated the benefits of Apple Silicon, including:

- ARM-based efficiency
- Unified Memory Architecture
- SSD storage performance
- Low CPU utilization under normal workloads
- Advanced memory management through compression and swap mechanisms

The lab also highlighted the trade-off between modern system integration and hardware upgradeability, providing valuable insight into current computer hardware design principles.
