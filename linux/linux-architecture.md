# Linux Fundamentals - Module 1

# Linux Architecture

## Learning Objectives

After completing this module, you will understand:

- What Linux actually is
- Difference between Linux and Ubuntu
- Linux Kernel
- Linux Distribution
- Shell
- Bash
- Terminal
- Linux Architecture
- Internal Working
- Real-world Cloud Relation
- Interview Questions
- Hands-on Practice

---

# 1. What is Linux?

Most beginners say:

> Linux is an Operating System.

This answer is technically incomplete.

Linux itself is **not a complete Operating System**.

Linux is an **Open Source Kernel**.

An Operating System is created by combining:

- Linux Kernel
- GNU Utilities
- Shell
- Package Manager
- System Libraries
- Applications

Example:

Linux Kernel
+
GNU Tools
+
APT
+
Bash

↓

Ubuntu

Similarly,

Linux Kernel
+
YUM/DNF

↓

RedHat

Linux Kernel
+
Amazon Packages

↓

Amazon Linux

Therefore,

Ubuntu, Debian, RedHat, CentOS and Amazon Linux are called **Linux Distributions**.

---

# 2. What is Kernel?

Kernel is the **core component** of an Operating System.

It acts as a bridge between applications and hardware.

Without the Kernel, software cannot communicate with hardware.

Applications never access hardware directly.

Instead,

Application

↓

Kernel

↓

Hardware

Example

Chrome Browser

↓

Kernel

↓

CPU

or

VS Code

↓

Kernel

↓

SSD

or

Python Program

↓

Kernel

↓

RAM

---

# 3. Responsibilities of Kernel

The Linux Kernel manages almost every hardware resource.

### CPU Management

- Process Scheduling
- Context Switching
- CPU Time Allocation

---

### Memory Management

- RAM Allocation
- Virtual Memory
- Swap Memory
- Memory Protection

---

### Process Management

- Create Process
- Terminate Process
- Process Scheduling
- Process Communication

---

### Filesystem Management

- Read Files
- Write Files
- Delete Files
- Permissions
- Mount Filesystems

---

### Device Management

Handles communication with:

- Keyboard
- Mouse
- SSD/HDD
- Network Interface Card
- USB Devices

using Device Drivers.

---

### Network Management

Kernel manages

- TCP
- UDP
- Sockets
- Network Interfaces
- Packet Routing

---

### Security

Kernel provides

- User Isolation
- Permission Enforcement
- Access Control

---

# 4. Why do we need a Kernel?

Imagine there is no Kernel.

Every application would need to know:

- How CPU works
- How RAM works
- How SSD stores data
- How Network Card sends packets

This is impossible.

Kernel abstracts all hardware complexity.

Applications simply ask the Kernel.

---

# 5. Linux Distribution

Linux Distribution (Distro) is a complete Operating System built around the Linux Kernel.

Examples

- Ubuntu
- Debian
- RedHat Enterprise Linux
- CentOS
- Rocky Linux
- AlmaLinux
- Amazon Linux
- SUSE Linux

Cloud Engineers commonly work with:

- Ubuntu
- Amazon Linux
- RedHat

---

# 6. Shell

A Shell is a command interpreter.

It acts as an interface between the User and the Linux Kernel.

Example

User types

ls

↓

Shell

↓

Kernel

↓

Filesystem

↓

Shell

↓

Output

---

# 7. Bash

Bash stands for

Bourne Again SHell

It is the default shell on Ubuntu.

Other popular shells:

- sh
- zsh
- fish
- ksh

---

# 8. Terminal

Many beginners confuse Terminal and Shell.

Terminal is simply a program (window) used to interact with the Shell.

Examples

- GNOME Terminal
- Windows Terminal
- iTerm2

Flow

User

↓

Terminal

↓

Shell

↓

Kernel

↓

Hardware

---

# 9. Linux Architecture

```
+---------------------------+
|      Applications         |
+---------------------------+
|      Shell (Bash)         |
+---------------------------+
|      Linux Kernel         |
+---------------------------+
|        Hardware           |
+---------------------------+
```

---

# 10. Real World Cloud Example

You launch an EC2 Instance.

Internally

EC2

↓

Ubuntu

↓

Linux Kernel

↓

AWS Hypervisor

↓

Physical Hardware

When you execute

docker ps

Flow becomes

User

↓

Bash

↓

Kernel

↓

Docker Engine

↓

Containers

---

# 11. Hands-on Commands

Check Kernel Version

```bash
uname -a
```

---

Check Linux Distribution

```bash
cat /etc/os-release
```

---

Check Current Shell

```bash
echo $SHELL
```

---

System Information

```bash
hostnamectl
```

---

Current User

```bash
whoami
```

---

# 12. Interview Questions

### Q1. What is Linux?

### Q2. What is Kernel?

### Q3. Difference between Linux and Ubuntu?

### Q4. What is a Linux Distribution?

### Q5. What is Shell?

### Q6. Difference between Shell and Terminal?

### Q7. Responsibilities of Linux Kernel?

### Q8. Why do Docker containers use the Host Kernel?

### Q9. Can Linux run without Bash?

### Q10. What happens internally when you execute the ls command?

---

# 13. Key Takeaways

- Linux is a Kernel.
- Ubuntu is a Linux Distribution.
- Kernel communicates with Hardware.
- Shell communicates with Kernel.
- Bash is one type of Shell.
- Terminal is only a program used to access the Shell.
- Every Cloud Service running Linux depends on the Linux Kernel.

---

# Module Completion Checklist

- [ ] Linux vs Ubuntu
- [ ] Kernel
- [ ] Linux Distribution
- [ ] Shell
- [ ] Bash
- [ ] Terminal
- [ ] Linux Architecture
- [ ] Hands-on Commands
- [ ] Interview Questions