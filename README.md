# Enterprise-Network-Infrastructure-Design-for-SME-Office

## 📌 Overview

This project presents a complete network infrastructure design for a small-to-medium enterprise (SME) office environment. The design focuses on scalability, security, and performance, supporting approximately 50 staff members, guest users, and network devices.

The solution addresses limitations in legacy networks by introducing structured VLAN segmentation, centralized management, and high-performance wireless connectivity.

---

## 🎯 Objectives

* Design a scalable and secure LAN and WLAN architecture
* Implement VLAN-based segmentation for traffic isolation
* Provide reliable Wi-Fi coverage using Wi-Fi 6
* Secure the network using a Next-Generation Firewall (NGFW)
* Enable centralized monitoring and management

---

## 🏗️ Network Architecture

The network follows a hierarchical design model:

* **Edge Layer:** Next-Generation Firewall (NGFW)
* **Core Layer:** Layer 3 Aggregation Switch
* **Access Layer:** Layer 2 PoE+ Switches
* **Wireless Layer:** Wi-Fi 6 Access Points with centralized controller

> The firewall performs inter-VLAN routing and acts as the default gateway for all VLANs.

---

## 🌐 VLAN Design

| VLAN ID | Name            | Subnet          | Purpose                     |
| ------- | --------------- | --------------- | --------------------------- |
| 10      | Staff           | 192.168.10.0/24 | Employee devices            |
| 20      | Admin           | 192.168.20.0/24 | IT/admin systems            |
| 30      | Network Devices | 192.168.30.0/24 | Switches, APs, management   |
| 40      | Guest           | 192.168.40.0/24 | Guest Wi-Fi (internet-only) |
| 50      | IoT / Printers  | 192.168.50.0/24 | Printers and IoT devices    |

---

## 📡 Wireless Network Design

* 8 × Wi-Fi 6 Access Points (4 per floor)
* Controller-based centralized management
* Separate SSIDs:

  * Corporate (VLAN 10)
  * Guest (VLAN 40)
  * IoT (VLAN 50)
* Optimized coverage with roaming support
* Channel planning to minimize interference

---

## 🔐 Security Implementation

* Next-Generation Firewall (NGFW) for traffic control and NAT
* VLAN segmentation to isolate network segments
* WPA2/WPA3-Enterprise authentication for corporate Wi-Fi
* Captive portal for guest access
* 802.1X authentication for wired devices
* DHCP Snooping and Dynamic ARP Inspection (DAI)
* VPN access with Multi-Factor Authentication (MFA)

---

## ⚙️ Key Features

* Inter-VLAN routing handled at the firewall
* QoS support for voice and video traffic
* Centralized monitoring using SNMP-based tools
* High Availability (HA) design option
* Structured cabling using Cat6A

---

## 🛠️ Technologies Used

* Cisco Catalyst Switches (Layer 2/Layer 3)
* Fortinet NGFW (conceptual design)
* VLAN (IEEE 802.1Q)
* DHCP / DNS
* SNMP (Network Monitoring)
* WPA2/WPA3 Wireless Security

---

## 📊 Project Structure

```
network-infrastructure-design/
│
├── docs/        # Design documentation
├── diagrams/    # Network diagrams (topology, VLAN, WLAN)
├── configs/     # Sample network configurations
├── appendix/    # IP addressing, device tables
└── assets/      # Floor plans and supporting images
```

---

## 📈 Budget Summary

* **Total Estimated Cost:**

  * USD: $29,800
  * LKR: 8,940,000

Includes core infrastructure, access layer, wireless deployment, and cabling.

---

## 🚀 Key Learning Outcomes

* Designing scalable enterprise network architectures
* Implementing VLAN-based segmentation
* Understanding real-world security controls
* Planning wireless coverage and performance
* Applying networking concepts to practical scenarios

---

## ⚠️ Disclaimer

This project was originally developed as part of an academic assignment and has been refined for portfolio purposes. Certain implementation details may be generalized or omitted. The design reflects real world networking principles but is presented as a conceptual implementation.
---

## 👤 Team

- **Sithira Chandrasiri**  
- **Rumesha Nisadi**  
- **Sesath Rathnayaka**  
- **Sasmi Premathilaka**


