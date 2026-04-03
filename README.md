📘 README: Configuring a DHCP Server in Cisco Packet Tracer

📌 Project Title

Configuring a DHCP Server in Cisco Packet Tracer

🎯 Objective

This lab demonstrates how to configure a centralized DHCP (Dynamic Host Configuration Protocol) server to automatically assign IP addresses to multiple devices within a Local Area Network (LAN).

By completing this lab, you will learn to:

Build a basic star-topology network
Assign a static IP address to a server
Configure a DHCP service pool
Obtain dynamic IP addresses on client devices
🖥️ Network Setup
Devices Used
1 × Switch (2960)
3 × PCs (PC0, PC1, PC2)
1 × Server (Server0)
Topology

A star topology is used where all devices are connected to a central switch.

Connections
Server0 → Switch0 (Fa0/1)
PC0 → Switch0 (Fa0/2)
PC1 → Switch0 (Fa0/3)
PC2 → Switch0 (Fa0/4)

⚙️ Configuration Steps

1️⃣ Server Static IP Configuration

The server must have a fixed IP before acting as a DHCP server.

IP Address: 192.168.1.1
Subnet Mask: 255.255.255.0

2️⃣ DHCP Configuration

The server is configured to assign IP addresses automatically.

Service: ON
Pool Name: serverPool
Start IP Address: 192.168.1.2
Subnet Mask: 255.255.255.0
Default Gateway: 0.0.0.0
DNS Server: 0.0.0.0
Maximum Users: 255

3️⃣ Client Configuration

Each PC is configured to obtain an IP address dynamically:

Set IP Configuration to DHCP
Devices automatically receive IP addresses (e.g., 192.168.1.x)

✅ Verification and Testing
Commands Used

Run the following command in Command Prompt:

ipconfig

To test connectivity:

ping <IP_of_PC1>
ping <IP_of_PC2>
ping 192.168.1.1
Expected Result
All devices should successfully communicate
Ping results should show 0% packet loss


📚 Conclusion
This lab successfully demonstrates how a DHCP server simplifies network management by automatically assigning IP addresses to devices, reducing manual configuration and errors.
