Cisco Packet Tracer Lab - Troubleshooting Static Routes

Description

This lab is a network simulation created in Cisco Packet Tracer, focusing on troubleshooting static routes and resolving misconfigurations. The topology includes two routers, switches, and PCs, where connectivity issues exist due to incorrect configurations.

Devices Used:

Cisco 2911 Routers (R1, R2)

Cisco 2960 Switches (SW1, SW2)

PCs (PC1, PC2)

Network Structure:

Three subnetworks with assigned IP addresses:

192.168.1.0/24 (PC1 and SW1)

192.168.3.0/24 (PC2 and SW2)

192.168.12.0/24 and 192.168.13.0/24 (Inter-router communication)

Routers should be correctly configured to enable communication between PCs.

Objectives

Identify and resolve misconfigurations on R1 and R2.

Correctly assign and verify IP addresses on router interfaces.

Configure static routes on R1 and R2 to enable full connectivity.

Test network connectivity by pinging PC2 from PC1.

Setup Instructions

Open the .pkt file in Cisco Packet Tracer.

Examine the existing configuration using show running-config and show ip route.

Identify misconfigurations on R1 and R2.

Correct the IP addressing or routing issues on the routers.

Configure the necessary static routes to enable connectivity.

Verify interface status using show ip interface brief.

Save the corrected configuration using write memory.

Test connectivity by pinging PC2 from PC1.

If pings fail, recheck IP addressing, subnet masks, and routes.

Screenshot



Notes

Ensure that each PC’s gateway is set correctly.

If pings fail, verify that static routes are correctly configured and match the expected network topology.

Author

Created for educational purposes in Cisco Networking Labs.


