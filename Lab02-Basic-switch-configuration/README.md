# Lab02 – Basic Switch Configuration (Cisco Packet Tracer)

## 🎯 Objective
Configure a Cisco switch with basic security hardening and management access.  
This includes hostname, console password, enable secret, banner, and SVI interface.

---

## 🧩 Topology

[PC] ---- [SW-02]

Single PC connected to FastEthernet0/1 on the switch.

---

## 🛠️ Step-By-Step Configuration

### 1️⃣ Configure Hostname

enable
configure terminal
hostname SW-02

---

### 2️⃣ Secure Console Access

line console 0
password cisco123
login
exit

---

### 3️⃣ Set Enable Secret password

enable secret admin123

---

### 4️⃣ Add Security Banner (MOTD)

banner motd #Unauthorized access is prohibited#

---

### 5️⃣ Configure Management Interface (VLAN 1)

interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

---

### 6️⃣ Save Configuration

copy running-config startup-config

---

## 🧪 Verification Commands

### ✔ Show running configuration

show running-config

![Running Config](screenshots/config.PNG)

### ✔ Check VLANs

show vlan brief

![VLAN Brief](screenshots/vlan.PNG)

### ✔ Check Interface Status

show interfaces status

![Interface Status](screenshots/int-status.PNG)

### ✔ Check SVI

show ip interface brief

![IP Interface Brief](screenshots/ip-int.PNG)

### ✔ Ping Test (PC → Switch)
From the PC:

ping 192.168.1.1

![PC0 Ping](screenshots/pc0-ping.PNG)

Result: 100% success.

---

## 📦 Files Included
- `lab02.pkt`
- `README.md`
- `screenshots/`

---

## 🏁 Result
Switch successfully configured for:
- Local access security  
- Management IP  
- Operational VLAN interface  
- Verified connectivity  

Lab02 **completed successfully**.

---
