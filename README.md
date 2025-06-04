Network Infrastructure Design Project

This repository contains the configuration and documentation for a secure mid-sized enterprise network simulation using **Cisco Packet Tracer**, as part of the Internet Programming subject (Final Submission).

---

## 🔖 Project Title
**Design and Implement a Network Infrastructure with VLANs, DHCP Servers, Firewalls, and Internet Connectivity**

---

## 🎯 Objective

Design and configure a secure and segmented network for a mid-sized company using Cisco Packet Tracer. Key elements include:

- VLAN configuration for departmental separation
- DHCP servers for dynamic IP allocation
- Access Control Lists (ACLs) as firewalls to enforce inter-VLAN communication rules
- NAT and routing for full internet connectivity

---

## 📁 Contents

- `router-config.txt` – Configuration commands for internal and ISP routers
- `packet-tracer.pkt` – The Cisco Packet Tracer project file (add your file here)
- `README.md` – Project overview and instructions

---

## 🧱 Network Features

### ✅ VLANs
- VLAN 10 – Guest
- VLAN 20 – Guest
- VLAN 30 – Guest
- VLAN 40 – Admin
- VLAN 50 – Admin
- VLAN 60–70 – Reserved
- VLAN 80 – Emergency

### ✅ Access Control Lists
- Restricted communication between guest and admin VLANs
- Emergency VLAN can reach others but is isolated from inbound communication
- VLAN 40 ↔ VLAN 50 restricted by ACLs

### ✅ NAT & Internet
- ISP Router provides NAT overload (PAT) for simulated internet access
- Internal router handles dynamic NAT for private VLAN subnets
- Static routes ensure end-to-end connectivity

---

## 🚀 How to Run

1. Open the `packet-tracer.pkt` file in **Cisco Packet Tracer**
2. Apply the router commands from `router-config.txt` or copy them directly into device CLIs
3. Verify connectivity using:
   ```bash
   show ip route
   ping 203.0.113.1

