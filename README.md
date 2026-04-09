# Enterprise Network Security & Segmentation Lab
**Author:** SoSerious416
**Status:** Completed (Simulation Phase)

## 📌 Project Overview
A simple multi-layered enterprise network design implemented in Cisco Packet Tracer. The project focuses on the **Three-Tier Hierarchical Model** (Core, Distribution, Access)

## 🏗️ Architecture
- **Core Layer:** Multilayer Switch (3560) handling Inter-VLAN routing and SVI management.
- **Distribution Layer:** Redundant 2960 switches.
- **Access Layer:** VLAN-specific port assignments for End-Devices.
- **Management:** Centralized WLC for Wireless infrastructure and dedicated DHCP/DNS servers.

## 🛡️ Security Features
- **Network Segmentation:** Isolated VLANs (Staff, Bank, Management) using Extended ACLs.
- **Honeypot Decoy (VLAN 50):** A dedicated "Blackhole" subnet designed to attract and log unauthorized reconnaissance.
- **Wireless Security:** WPA2-Enterprise authentication via the WLC.
- **Edge Security:** ISR4331 Router acting as the gateway to the ISP/Internet.

## 📊 IP Addressing Schema
| VLAN | Description | Subnet | Gateway |
| :--- | :--- | :--- | :--- |
| 10  | Staff      | 192.168.10.0/24  | 192.168.10.1  |
| 20  | Bank       | 192.168.20.0/24  | 192.168.20.1  |
| 50  | Honeypot   | 192.168.50.0/24  | 192.168.50.1  |
| 99  | Management | 192.168.99.0/24  | 192.168.99.1  |
| 200 | Wifi       | 192.168.200.0/24 | 192.168.200.1 |

## 🚀 How to Run
1. Download the `.pkt` file from this repository.
2. Open with **Cisco Packet Tracer (v8.2 or higher)**.
3. Use the **Simulation Mode** to track ICMP packets across subnets.

**NOTE** : Run python scripts on your preferneces
