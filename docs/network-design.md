# Network Design

## Architecture Overview

The network follows a hierarchical design:

- Edge Layer: Next-Generation Firewall
- Core Layer: Layer 3 Aggregation Switch
- Access Layer: Layer 2 PoE+ Switches

## VLAN Design

| VLAN ID | Name            | Purpose                  |
|--------|-----------------|--------------------------|
| 10     | Staff           | Employee devices         |
| 20     | Admin           | IT/admin systems         |
| 30     | Network Devices | Switches, APs, mgmt      |
| 40     | Guest           | Guest Wi-Fi users        |
| 50     | IoT             | Printers, smart devices  |

## IP Addressing

- VLAN 10: 192.168.10.0/24
- VLAN 20: 192.168.20.0/24
- VLAN 30: 192.168.30.0/24
- VLAN 40: 192.168.40.0/24
- VLAN 50: 192.168.50.0/24

## Switching Design

- Aggregation switch located in MDF
- Two access switches (one per floor)
- Trunk links using 802.1Q tagging
- Link aggregation (LACP) for redundancy

## Wireless Design

- 8 Wi-Fi 6 Access Points (4 per floor)
- Controller-based management
- SSIDs mapped to VLANs

## High Availability (Optional)

- Dual firewall setup
- Redundant uplinks
- Failover support
