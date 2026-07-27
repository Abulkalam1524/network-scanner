# 🔍 Network Scanner

![Python](https://img.shields.io/badge/Python-3.x-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Windows-lightgrey)

A simple Python tool that scans a local network to discover connected devices, displaying each device's **IP address** and **MAC address**. Built using **Scapy**, this project demonstrates how ARP requests work at the network layer.

---

## 📋 Table of Contents
- [Features](#-features)
- [Requirements](#-requirements)
- [Installation](#-installation)
- [Usage](#-usage)
- [How It Works](#-how-it-works)
- [Demo](#-demo)
- [Disclaimer](#-disclaimer)

---

## ✨ Features
- Scans a target IP or IP range using ARP requests
- Displays IP and MAC address of every responding device
- Lightweight — no external scanning tools required, pure Python + Scapy
- Beginner-friendly code with clear structure

## ⚙️ Requirements
- Python 3.x
- [Scapy](https://scapy.net/) library
- Administrator / root privileges
- **Windows users:** [Npcap](https://npcap.com/) must be installed (Scapy depends on it for packet capture)

## 📦 Installation

```bash
git clone https://github.com/Abulkalam1524/network-scanner.git
cd network-scanner
pip install scapy
```

## 🚀 Usage

```bash
sudo python3 network_scanner.py -t <target_ip_or_range>
```

**Example:**
```bash
sudo python3 network_scanner.py -t 192.168.1.1/24
```

**Sample Output:** ## 🧠 How It Works
1. Builds an ARP request packet targeting the given IP range.
2. Wraps it in an Ethernet broadcast frame (`ff:ff:ff:ff:ff:ff`) so it reaches every device on the local network.
3. Sends the packet and listens for replies using `scapy.srp()`.
4. Extracts the IP and MAC address from each device that responds.
5. Prints the results in a clean table format.

## 📸 Demo

<img width="640" height="226" alt="image" src="https://github.com/user-attachments/assets/ff1adc2b-6057-4934-8276-b6faa8150e7d" />


## ⚠️ Disclaimer
This project was built for **educational purposes only**, as part of learning Python and ethical hacking fundamentals. Only scan networks you **own** or have **explicit permission** to test. Unauthorized network scanning may be illegal in your jurisdiction.

---

### 🔗 Related Projects
- [MAC Address Changer](https://github.com/Abulkalam1524/mac-address-changer)
