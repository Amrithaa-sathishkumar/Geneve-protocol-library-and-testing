# GENEVE Protocol Library (IPv4 & IPv6 Support)

This project provides a multithreaded implementation of the **GENEVE (Generic Network Virtualization Encapsulation)** protocol using **C**. It supports sending and receiving **GENEVE-encapsulated packets** over **IPv6**, with full inner packet encapsulation (Ethernet + IPv4 + UDP + Payload).

## ✨ Features

-  Create and parse GENEVE headers
-  Encapsulate and decapsulate:
-  Outer Ethernet + IPv6 + UDP headers
-  GENEVE header
-  Inner Ethernet + IPv4 + UDP + Payload
-  Compute correct UDP checksums
-  Use port `6081` (standard GENEVE UDP port)
-  Multithreaded simulation of sending and receiving GENEVE packets

## 📁 Project Structure

from pathlib import Path

# Content of the directory structure as requested
directory_structure = """geneve/
├── include/
│   └── geneve.h             # GENEVE protocol definitions
├── src/
│   └── geneve.c             # GENEVE implementation logic
├── test/
│   └── geneve_test4.c        # Test program with multithreaded send/recv for ipv4
│   └── geneve_test6.c        # Test program with multithreaded send/recv for ipv6
├── Makefile                 # Build configuration
└── README.md                # Project documentation
"""

# Save the structure to a text file
file_path = Path("/mnt/data/geneve_structure.txt")
file_path.write_text(directory_structure)

file_path.name


## ⚙️ Requirements

- Linux OS (tested on Ubuntu)
- GCC or Clang
- Root privileges (for raw socket access)
- Network interface (e.g., `enp3s0` or `eth0`)
- Proper IPv6 setup between two systems

## 🛠️ Build Instructions

To compile the project:

```bash
make
