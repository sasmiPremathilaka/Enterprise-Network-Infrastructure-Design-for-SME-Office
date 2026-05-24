# VLAN & IP Addressing Scheme

## VLAN Configuration Table

| VLAN ID | Name              | Subnet              | Gateway        | DHCP Scope     | Purpose |
|--------|------------------|---------------------|----------------|----------------|---------|
| 10     | Staff            | 192.168.10.0/24     | 192.168.10.1   | .10 - .200     | Staff PCs, laptops, corporate wireless |
| 20     | Admin            | 192.168.20.0/24     | 192.168.20.1   | .10 - .50      | IT admin systems and management |
| 30     | Network Devices  | 192.168.30.0/24     | 192.168.30.1   | Static only    | Switches, APs, management interfaces |
| 40     | Guest            | 192.168.40.0/24     | 192.168.40.1   | .10 - .150     | Guest Wi-Fi users (internet-only) |
| 50     | IoT / Printers   | 192.168.50.0/24     | 192.168.50.1   | .10 - .60      | Printers and IoT devices |
| 99     | Native / Unused  | N/A                 | N/A            | None           | Reserved VLAN for trunk links |

---

## DHCP & DNS Configuration

| VLAN | DHCP Scope                | DNS (Primary)              | DNS (Secondary) | Lease Time |
|------|--------------------------|----------------------------|------------------|------------|
| 10   | 192.168.10.50 - .200     | 192.168.10.1 (NGFW)        | 8.8.8.8          | 24 hours   |
| 20   | 192.168.20.20 - .50      | 192.168.20.1 (NGFW)        | 8.8.8.8          | 24 hours   |
| 30   | Static only              | 192.168.30.1 (NGFW)        | —                | N/A        |
| 40   | 192.168.40.10 - .150     | 192.168.40.1 (filtered)    | —                | 4 hours    |
| 50   | 192.168.50.20 - .60      | 192.168.50.1 (NGFW)        | —                | 8 hours    |
