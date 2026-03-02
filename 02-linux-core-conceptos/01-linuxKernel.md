# 02 Linux Core Conceptos

## Bob's first team meeting

## Linux Kernel

### Linux Core Conceptos

#### Introduction To the Linux Kernel

Application / Process <---> Linux Kernel <---> (Memory) (CPU) (DEVICES)

```console
    uname
    Linux

    uname -r
    6.6.87.2-microsoft-standard-WSL2
```

#### Kernel Space and User Space

##### Kernel Space
- Kernel
- Device Drivers

(Kernel Code, Kernel Extension, Device Drivers)


#### User Space
- Application / Programs

(C, Java, Python, Ruby)


#### FLOW
HARDAWRE <----- KERNEL SPACE <-- SYSTEM CALLS --- USER SPACE (Open a File, Write to a File, List Processes, Defining a variable)

# Linux Core Concepts: Kernel and System Calls

In Linux, there is a clear separation between the user and the hardware. This is how the system is organized:

---

## 1. User Space
This is the "safe" area where our applications run (like Python, Chrome, or the Terminal). 
* **Note:** Applications here cannot touch the hardware directly.
* **Task example:** Defining a variable (`x = 10`) happens only here.

## 2. System Calls (The Middleware)
A **System Call** (or *syscall*) is the bridge between the User Space and the Kernel.
* **Role:** It acts as the **middleware**. 
* **When is it used?** When an app needs to "talk" to the hardware.
* **Common examples:** `open()` a file, `write()` to a disk, or `start` a new process.

## 3. The Kernel (The Orchestrator)
The **Kernel** is the heart of the Operating System. 
* **Role:** It is the **resource manager** or **orchestrator**.
* **Main tasks:** * Managing CPU time.
    * Allocating Memory (RAM).
    * Controlling Hardware (Disk, Network, Keyboard).

## 4. Hardware
The physical components: CPU, RAM, and SSD/HDD.

---

### Summary Diagram
**USER SPACE** (App) 
      ↓ 
**SYSTEM CALLS** (Middleware / Request) 
      ↓ 
**KERNEL SPACE** (Orchestrator / Logic) 
      ↓ 
**HARDWARE** (Physical execution)

#### Working with hardware

```console
    dmesg

    dmesg | grep -i usb
```

```console
    udevadm info --query=path --name=/dev/sda5
    Unknown device "/dev/sda5": No such device

    udevadm monitor
    monitor will print the received events for:
    UDEV - the event which udev sends out after rule processing
    KERNEL - the kernel uevent
```

```console
    lspci
```

```console
    lsblk
NAME
    MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
    sda   8:0    0 388.6M  1 disk
    sdb   8:16   0   186M  1 disk
    sdc   8:32   0     4G  0 disk [SWAP]
    sdd   8:48   0     1T  0 disk /mnt/wslg/distro
                                /
```

```console
    lscpu
    Architecture:             x86_64
    CPU op-mode(s):         32-bit, 64-bit
    Address sizes:          39 bits physical, 48 bits virtual
    Byte Order:             Little Endian
    CPU(s):                   4
    On-line CPU(s) list:    0-3
    Vendor ID:                GenuineIntel
    Model name:             Intel(R) Core(TM) i5-6600K CPU @ 3.50GHz
        CPU family:           6
        Model:                94
        Thread(s) per core:   1
        Core(s) per socket:   4
```

```console
    lsmem --summary
    Memory block size:       128M
    Total online memory:      16G
    Total offline memory:      0B

    free -m
               total        used        free      shared  buff/cache   available
    Mem:           15969        1066       14800           3         323       14902
    Swap:           4096           0        4096
```

```console
    lshw
    WARNING: you should run this program as super-user.
    getsemani
        description: Computer
        width: 64 bits
        capabilities: smp vsyscall32
    *-core
        description: Motherboard
        physical id: 0
        *-memory
```

#### Labs: Linux Core Concepts

#### Linux Boot Sequence

#### SYSTEMD TARGETS (RUNLEVELS)

#### Filesystems and Hierarchy

## Working Hardware

## Lab: Linux Kernel

## Linux Boot Requence

## Runelevels

## Article: Runlevels

## File Types

## Filesystem hierarchy

## Lab: Linux modules boot and filetypes

# Linux Boot Sequence

## Sequence Overview

BIOS POST -> Boot Loader (GRUB2) -> Kernel Initialization -> Init Process (SystemMD)

# Runlevels

```console
    runlevel
```

Systemd Target (Runlevels)
5 -> Graphical.target -> Boots into a graphical Interface
3 -> Multiuser.target -> Boots into a command line interface

The term runlevels is used in the sysV init systems. These have been replaced by systemd targets in systemd based systems.

The complete list of runlevels and the corresponding systemd targets can be seen below:

runlevel 0 -> poweroff.target

runlevel 1 -> rescue.target

runlevel 2 -> multi-user.target

runlevel 3 -> multi-user.target

runlevel 4 -> multi-user.target

runlevel 5 -> graphical.target

runlevel 6 -> reboot.target

```console
    systemctl get-default
    graphical.target

    ls -ltr /etc/systemd/system/default.target
```

# File Types

File Types in linux

Regular File -> Images, Scripts, Configuration / Data Files
Directory -> /home/bob, /root, /home/bob, /code/directory
Special Files -> Character Files, Block Files, Links (hard Link, Soft Links), Socker Files, Named Pipes

# FileSystem Hierarchy

