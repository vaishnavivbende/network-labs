# Lab 01 — Basic PC to Switch Connectivity

## Objective
To establish a simple wired network connection between two PCs using a Cisco switch, and verify connectivity using `ping`.

---

## Topology
- PC0 connected to Switch using Copper Straight-Through cable
- PC1 connected to Switch using Copper Straight-Through cable

![Topology](screenshots/topology.PNG)

---

## Device List
| Device | Model | Count |
|--------|--------|-------|
| PC     | Generic | 2 |
| Switch | 2960 | 1 |
| Cable  | Copper Straight-Through | 2 |

---

## Configuration Steps

### Place Devices
- Add **2 PCs** and **1 Switch (2960)** to the workspace

### Cabling
- Use **Copper Straight-Through** cable to connect:
  - PC0 → Switch (FastEthernet0/1)
  - PC1 → Switch (FastEthernet0/2)

### Assign IP Addresses
PC0:

IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0

![PC0 IP Config](screenshots/PC0-ip.PNG)

PC1:

IP Address: 192.168.1.20
Subnet Mask: 255.255.255.0

![PC1 IP Config](screenshots/PC1-ip.PNG)

### Verify Connectivity
- From PC0 → Command Prompt:

ping 192.168.1.20

![PC0 Ping](screenshots/pc0-ping.PNG)

- From PC1:

ping 192.168.1.10

![PC1 Ping](screenshots/pc1-ping.PNG)

Successful ping = **network connectivity established**

---

## Switch MAC Address Table
Command:

Switch> show mac address-table

Switch learns MAC addresses dynamically as frames are forwarded.

![MAC Table](screenshots/mac-table.PNG)

---

## Switch Interface Status
Command:

Switch> show ip interface brief

Shows connected ports up/up.

![IP Interface](screenshots/ip-interface.PNG)

---

## Outcome
- PCs can communicate through the switch
- MAC learning verified
- Basic LAN setup completed successfully

---

## Files Included
- `lab01.pkt`
- `README.md`
- `screenshots/`

---

Lab01 **completed successfully**
