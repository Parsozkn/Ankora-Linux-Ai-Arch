<div align="center">
  <img src="https://raw.githubusercontent.com/Parsozkn/Ankora-Linux/main/Ankora%20G%C3%BCncel%20Logo.jpg" alt="Ankora OS Logo" width="220" style="border-radius: 50%;">
</div>

<p align="left">
  <img src="https://img.shields.io/badge/VERSION-2.0_(EMERALD)-0085d1?style=for-the-badge&labelColor=383838" alt="Version">
  <img src="https://img.shields.io/badge/BASE-ARCH_LINUX-1793d1?style=for-the-badge&labelColor=383838" alt="Base">
  <img src="https://img.shields.io/badge/DESKTOP-XFCE_%7C_KDE-0085d1?style=for-the-badge&labelColor=383838" alt="Desktop">
  <img src="https://img.shields.io/badge/LICENSE-OPEN_SOURCE-41a013?style=for-the-badge&labelColor=383838" alt="License">
</p>

# Ankora Linux AI Arch (Ankora OS - AI Arch Edition)

Ankora OS AI Arch is a modern Linux distribution project based on Arch Linux, adopting the rolling release model, and focusing on high performance, responsiveness, and stability. The system comes equipped with a local (offline) AI assistant integrated directly into the terminal and developer-focused utilities.

[🇹🇷 Türkçe README için tıklayın (Click here for Turkish)](README.md)

---

## 📌 What is Ankora OS AI Arch?

Ankora OS AI Arch combines the bleeding-edge package ecosystem and flexibility of Arch Linux with Ankora's optimized kernel parameters and local AI integration. The system is free of telemetries and heavy background workloads, utilizing hardware resources with maximum efficiency.

The built-in offline AI assistant, called via the `yardimci` command, requires no external cloud servers or API keys. It runs entirely on local machine resources to provide instant command-line reference, troubleshooting, and system analysis.

---

## 🛠 Key Engineering Choices and Architecture

### 1. Arch Linux & Rolling Release
* **Always Up-to-Date:** Instant access to the latest Linux kernels, drivers, and software packages.
* **AUR Support:** Access to thousands of community-maintained packages via the Arch User Repository (AUR).

### 2. Offline Terminal AI Assistant (`yardimci`)
The AI utility is called in the terminal with the `yardimci` command:
* Completely private—no data is sent to external servers; everything is processed locally on your machine.
* Generates quick and smart solutions for shell commands, package management, configuration mistakes, and code snippets.

### 3. Advanced Memory Management (ZRAM + SWAP)
* **ZRAM Integration:** Creates compressed swap space directly in RAM to minimize disk I/O latency and prevent system freezes during heavy workloads or gaming.
* **vm.swappiness & Cache Pressures:** Tweaked kernel parameters ensure rapid response rates and optimal memory caching.

### 4. Custom Ankora Utilities
Built-in local tools designed for seamless system maintenance:
* `ankora-backup`: An easy-to-use, quick system backup utility.
* `ankora-cleaner`: A utility to clear cache, old logs, and unused packages to keep the system clean.

### 5. Visual Consistency & Lightweight Desktop
* **XFCE & KDE Plasma:** Visual coherence with lightweight design, ensuring no duplicate helper apps are loaded (e.g., both desktop environments utilize **Dolphin** to avoid package bloat).
* **Fairy Wren Icon Theme:** Beautifully customized icon sets for an elegant aesthetic out of the box.
* **Bloat-Free Philosophy:** Bulky default office suites (like LibreOffice) are removed; you can install whatever you need with a single command.

---

## 📊 Release Comparison Table

| Edition | Base System | Release Type | Focus Area | Status |
| :--- | :--- | :--- | :--- | :--- |
| **Ankora AI Debian** | Debian 13 (Trixie) | Stable | High stability, extremely low resource footprint | **Active Release** |
| **Ankora AI Arch** | Arch Linux | Rolling Release | Bleeding-edge packages, custom tools (`ankora-backup`, `ankora-cleaner`) | **Active Testing / Dev** |
| **Ankora Enterprise** | Debian LTS | LTS | Centralized profiles, hardened security (AppArmor) | **Planning** |
| **Ankora Developer** | Debian / Arch | Custom Build | Compiler suites (GCC, Rust, Go, Python) and pre-configured Zsh terminal | **Special Release** |

---

## 📋 System Requirements

| Component | Minimum Requirement | Recommended System |
| :--- | :--- | :--- |
| **Processor (CPU)** | 64-bit Dual-Core (1.5 GHz) | 64-bit Quad-Core (2.0 GHz+) |
| **Memory (RAM)** | 2 GB (ZRAM Enabled) | 4 GB+ (8 GB+ recommended for running large local AI models) |
| **Storage** | 15 GB Free Disk Space | 25 GB SSD Storage |
| **Graphics (GPU)** | Any GPU with KMS support | Vulkan / OpenGL 4.5 capable GPU |

---

## ⚡ Installation and Usage Instructions

### 1. Flashing the ISO to a USB Drive
On Linux, you can create a bootable USB using the `dd` command:

```bash
sudo dd if=ankora-ai-arch-x86_64.iso of=/dev/sdX bs=4M status=progress conv=fsync
```

*(Please replace `/dev/sdX` with your actual USB device path.)*

### 2. Calamares Graphical Installer
Once booted into the Live Mode, double-click the **"Install Ankora OS"** icon on the desktop to start the user-friendly Calamares installation wizard.

---

## 🌐 Community and Support

Ankora OS is a community-driven open-source project. Feel free to contribute, report bugs, or share your thoughts:

* 💬 **Community Forum:** [Ankalab Flarum Cloud](https://ankalab.flarum.cloud)
* 🌍 **Official Website:** [ankora.xo.je](http://ankora.xo.je) 
* 🐞 **Bug Reports:** Open an issue via the GitHub [Issues](../../issues) tab or post on the forum.

---

### License & Source Code

Ankora OS AI Arch is built on top of **Arch Linux**. The base system, Linux Kernel, and upstream packages are distributed under their respective original open-source licenses (primarily GPL).

All custom configurations, desktop environments customizations, artwork, and scripts provided in this repository are licensed under the **MIT License**.
