# Requirements Analysis

## User and Device Requirements

- 50 staff users
- Up to 30 guest users
- Approximately 120 total endpoints

## Network Requirements

- 300 Mbps internet connection
- VLAN segmentation for security
- Secure remote access via VPN
- Centralized monitoring system

## Key Design Decisions

### VLAN Segmentation
- Staff VLAN
- Admin VLAN
- Guest VLAN
- IoT/Printer VLAN
- Network Devices VLAN

### Wireless Requirements
- Minimum -65 dBm coverage
- Support for roaming
- Separate SSIDs for staff and guests

### Security Requirements
- Firewall-based traffic control
- WPA2/WPA3 Enterprise authentication
- Guest isolation (internet-only access)

### Performance Requirements
- QoS for voice and video traffic
- Load distribution across access points
