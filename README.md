# Troubleshooting-Static-Routes
This lab challenges you to troubleshoot and fix static routing misconfigurations in a multi-router network. It is designed to test your ability to identify routing errors and restore end-to-end connectivity.
# 🛠️ Cisco Packet Tracer Lab – Troubleshooting Static Routes
![image](https://github.com/user-attachments/assets/62388a75-1b25-4a02-b846-044ce0f9cb24)

This lab challenges you to troubleshoot and fix static routing misconfigurations in a multi-router network. It is designed to test your ability to identify routing errors and restore end-to-end connectivity.

## 🧩 Lab Scenario

- **Issue:** PC1 and PC2 cannot ping each other.
- **Hint:** There is **one misconfiguration on each router**.
- **Goal:** Find and correct the misconfigurations to allow successful ping from PC1 to PC2.

## 🌐 Network Topology

- **Networks/Subnets:**
  - `192.168.1.0/24` — PC1’s LAN
  - `192.168.12.0/24` — Between R1 and R2
  - `192.168.13.0/24` — Between R2 and R3
  - `192.168.3.0/24` — PC2’s LAN
- **Routers:**
  - R1 ↔ R2 ↔ R3
- **Switches:** SW1, SW2 (no config required)
- **End Devices:** PC1, PC2

## 🔧 What to Do

1. Inspect static route configurations on R1, R2, and R3.
2. Identify incorrect next-hop addresses or network destinations.
3. Use CLI commands such as:
   - `show ip route`
   - `show running-config`
   - `ping` and `traceroute`
4. Fix the misconfigurations using `ip route` commands.

### Example Correction Command

```bash
R1(config)#no ip route 192.168.3.0 255.255.255.0 192.168.12.3
R1(config)#ip route 192.168.3.0 255.255.255.0 192.168.12.2
R2(config)#ip route 192.168.3.0 255.255.255.0 192.168.13.3
R2(config)#no ip route 192.168.3.0 255.255.255.0 g0/1
R2(config)#no ip route 192.168.3.0 255.255.255.0 g0/0
R3(config-if)#ip add 192.168.13.3 255.255.255.0

