# Bitcoin-Lightning-Node for RK322x

**How to run a Bitcoin Lightning node on devices using the RK322x ARM CPU.**  
Tested on LeefBox and other RK322x-based Android TV boxes running Armbian.

---

## ✅ Features
- **Bitcoin Core** (headless / no GUI)
- **Core Lightning (CLN)** for Lightning Network support
- Lightweight, works on ARMv7 single-board computers and TV boxes
- Ideal for **low-cost Lightning routing** or as a learning project

---

## 📋 Requirements
- RK322x-based device (e.g., LeefBox, MXQ Pro, M9S Pro)
- **Armbian Bookworm** (or compatible) installed  
  ➔ [https://github.com/armbian/community/releases](https://github.com/armbian/community/releases)
- 8GB+ SD card / eMMC / USB storage (preferably larger for better blockchain storage)
- Basic Linux knowledge
- Internet connection

---

## ⚙️ Installation Guide

### 1️⃣ Install Armbian
Use official Armbian builds or community-maintained versions for RK322x devices:  
[Armbian Community Builds](https://github.com/armbian/community/releases)

---

### 2️⃣ Build Bitcoin Core
```bash
sudo apt-get update
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git
sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev

git clone https://github.com/bitcoin/bitcoin.git
cd bitcoin
./autogen.sh
./configure --without-gui
make -j$(nproc)
sudo make install
