## 📌 Project Overview
This project is a comprehensive network topology design created for the **Computer Networking Fundamentals** course. It simulates a realistic campus/enterprise network infrastructure, featuring hierarchical routing, VLAN segmentation, wireless connectivity, and dedicated server zones.

## 🏗️ Network Architecture
The network is structured around a Core Switch (`CoreSW`) acting as the central distribution point, connecting various access switches, routers (`R1`, `R2`), and server farms.

### 1. VLAN Segmentation (Local Area Networks)
The internal network is divided into multiple VLANs to ensure security, reduce broadcast traffic, and organize departments logically:
* **VLAN 10 (IT Department / K.CNTT):** `192.168.10.0/24`
* **VLAN 20 (High-Quality Program / K.CLC):** `192.168.20.0/24`
* **VLAN 30 (Academic Affairs / P.DT):** `192.168.30.0/24`
* **VLAN 40 (Wi-Fi/Wireless Network):** `192.168.40.0/24`

### 2. Server Infrastructure
The topology includes two distinct server zones:
* **Internal Server Farm (`192.168.100.0/24`):** Hosts the **DHCP Server** (`.150`) for dynamic IP allocation and the **DNS Server** (`.160`) for internal domain resolution.
* **Public/External Services (`10.10.10.0/24`):** Separated via routers, this zone hosts external-facing services including a **WEB Server** (`.200`) and an **FTP Server** (`.100`) for the `XYZ.NET` domain.

### 3. Routing & Interconnectivity
* **Inter-VLAN Routing:** Managed by the Multilayer Core Switch (`CoreSW`).
* **Point-to-Point Links:** 
  * `CoreSW` to `R2`: `172.16.12.0/24`
  * `R2` to `R1`: `172.16.21.0/24`

## 🚀 Technologies & Concepts Demonstrated
* IPv4 Addressing and Subnetting
* VLAN Configuration & 802.1Q Trunking
* Inter-VLAN Routing (Layer 3 Switching)
* Static Routing
* Essential Network Services Setup (DHCP, DNS, HTTP, FTP)
* Wireless Access Point Integration

Topology 

<img width="789" height="477" alt="Screenshot 2026-06-22 183801" src="https://github.com/user-attachments/assets/c0664b23-1417-4a42-aaa7-c9f61e7942a8" />
