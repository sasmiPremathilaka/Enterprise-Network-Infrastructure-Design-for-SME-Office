# Security Design

## Threats Identified

- Malware via internet/email
- Unauthorized device access
- Rogue access points
- ARP spoofing attacks
- VPN brute-force attacks

## Security Controls

### Firewall (NGFW)
- Controls inter-VLAN traffic
- Enforces internet access policies
- Performs NAT and VPN termination

### VLAN Segmentation
- Isolates different user groups
- Prevents lateral movement of threats

### Wireless Security
- WPA2/WPA3 Enterprise for staff
- Captive portal for guest network
- IoT devices isolated

### Access Control
- 802.1X authentication
- MAC Authentication Bypass (MAB)

### Layer 2 Protection
- DHCP Snooping
- Dynamic ARP Inspection (DAI)
- Port security

### Monitoring
- SNMP-based monitoring system
- Syslog logging
