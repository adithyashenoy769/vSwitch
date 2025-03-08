# Virtual Network Switch (vSwitch)

A lightweight virtual network switch implementation that simulates Ethernet frame forwarding using **Linux TAP devices** and **UDP sockets**. Built to demonstrate core networking concepts like MAC address tables, packet forwarding, and broadcast handling.

---

## Features
- **Ethernet Frame Forwarding**: Simulates a real network switch by forwarding frames based on MAC addresses.
- **MAC Address Table**: Dynamically maps MAC addresses to virtual ports for efficient packet routing.
- **Broadcast Support**: Handles broadcast traffic (e.g., ARP requests) by forwarding frames to all connected ports.
- **TAP Device Integration**: Interfaces with Linux TAP devices to simulate real-world network interfaces.
- **Multi-threading**: Uses separate threads for sending and receiving packets, ensuring high performance.

---

## How It Works
1. **VSwitch**: The central hub that receives Ethernet frames from connected VPorts and forwards them based on the MAC address table.
2. **VPort**: Acts as a virtual network interface, connecting to the VSwitch via UDP sockets and interfacing with Linux TAP devices.
3. **Packet Handling**:  
   - Unicast: Frames are forwarded to the specific VPort associated with the destination MAC address.  
   - Broadcast: Frames are forwarded to all connected VPorts except the sender.  

---
