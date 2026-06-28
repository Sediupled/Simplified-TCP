# Simplified TCP (STCP)

> **A C-based networking project implementing a simplified version of the Transmission Control Protocol (TCP) for reliable data transfer.**

## 📖 Overview

**Simplified TCP** is a custom implementation of transport layer reliability mechanisms written in C. The project simulates real-world network conditions to test the robustness of data transmission against dropped, delayed, and corrupted packets. It includes custom state management and logging, featuring distinct sender and receiver executables tailored for both Linux and macOS environments.

## ✨ Features

* **Reliable Data Transfer:** Implements core TCP components and connection logic to ensure data integrity.
* **Custom Packet Management:** Handles packet queuing and sequence wrap-around handling utilizing `packet_list.c` and `wraparound.c`.
* **Network Anomaly Simulation:** Evaluates the connection against simulated delays (`delaysyn.script`), dropped packets (`dropsyn.script`), and probabilistic corruption (`probpointtwocorrupt.script`).
* **Comprehensive Testing Suite:** Includes automated test bash scripts such as `runallerrors.sh` and `runnoerrors.sh`, alongside granular C test files like `testtcp.c`.
* **Multi-Platform Receivers:** Provides distinct pre-compiled receiver binaries for Linux (`receiver_linux`), Intel-based Mac (`receiver_mac_intel`), and Apple Silicon Mac (`receiver_mac_apple`) systems.

## 🛠 Tech Stack

### Core Technologies

* **Language:** C
* **Build System:** Makefile
* **Logging:** Custom C-based logging utility (`log.c`, `log.h`)
* **Automation:** Bash shell scripts for test execution

## 🛣 Roadmap

* [ ] **Congestion Control:** Implement dynamic window scaling to handle high-latency environments.
* [ ] **Performance Optimization:** Refine packet parsing speed and minimize memory footprint in the event loop.
