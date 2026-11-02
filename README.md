# 🐧 Hermes Desktop for Linux

[![Sync and Build](https://github.com/dalroot/hermes-desktop-linux/actions/workflows/build-and-release.yml/badge.svg)](https://github.com/dalroot/hermes-desktop-linux/actions/workflows/build-and-release.yml)
[![GitHub Releases](https://img.shields.io/github/v/release/dalroot/hermes-desktop-linux?include_prereleases&color=blue&label=Latest%20Release)](https://github.com/dalroot/hermes-desktop-linux/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Native pre-built desktop packages (`.AppImage`, `.deb`, `.rpm`) and automated packaging pipeline for **Hermes Agent Desktop** by [Nous Research](https://github.com/NousResearch/hermes-agent).

---

## 💡 Why this exists

While [Hermes Agent](https://github.com/NousResearch/hermes-agent) provides official desktop installers for macOS (`.dmg`) and Windows (`.exe` / Microsoft Store), Linux users were previously required to manually clone the source repository, build Node/Electron runtimes, and configure system dependencies.

This repository automatically tracks upstream releases from `NousResearch/hermes-agent`, builds native standalone Linux packages with GitHub Actions, and distributes them immediately.

---

## 📦 Available Formats

| Format | Compatibility | Target Distributions |
| :--- | :--- | :--- |
| **`.AppImage`** | Universal / Standalone | Ubuntu, Debian, Fedora, Arch Linux, Manjaro, openSUSE, Alpine |
| **`.deb`** | Native Package Manager | Ubuntu, Debian, Linux Mint, Pop!_OS, Elementary OS |
| **`.rpm`** | Native Package Manager | Fedora, Red Hat Enterprise Linux, CentOS Stream, openSUSE |
| **AUR** | Arch User Repository | Arch Linux, Manjaro, EndeavourOS (`hermes-desktop-bin`) |

---

## 🚀 Installation & Usage

### 1. AppImage (Universal - Recommended)
No root or installation needed. Download, make executable, and run:
```bash
chmod +x Hermes-*-linux-x86_64.AppImage
./Hermes-*-linux-x86_64.AppImage
```

### 2. Ubuntu / Debian (`.deb`)
```bash
sudo dpkg -i Hermes-*-linux-amd64.deb || sudo apt-get install -f
```

### 3. Fedora / RHEL (`.rpm`)
```bash
sudo dnf install ./Hermes-*-linux-x86_64.rpm
```

### 4. Arch Linux (AUR)
```bash
yay -S hermes-desktop-bin
# or
paru -S hermes-desktop-bin
```

---

## ⚙️ Automated CI/CD Pipeline

* **Continuous Tracking:** A GitHub Actions workflow monitors `NousResearch/hermes-agent` releases on a recurring schedule.
* **Hermetic Actions:** Actions are pinned to full commit SHAs for supply chain security.
* **1:1 Upstream Parity:** Release notes, semantic versions, and tags match the exact official Nous Research releases.

---

## ⚖️ Upstream & Disclaimer

This is a community-maintained distribution packaging pipeline. All product rights, logos, and upstream codebase belong to [Nous Research](https://nousresearch.com).

* Upstream Repository: [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
* Maintainer: [Dal](https://github.com/dalroot)
