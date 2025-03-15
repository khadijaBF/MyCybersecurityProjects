#DNS Sniffer and ARP Spoofer

## Overview
This repository contains a Python script that performs **ARP Spoofing** to intercept and manipulate network traffic, combined with a **DNS Sniffer** to capture DNS requests. This script can be useful for network analysis, security auditing, or learning purposes.

The script works in two parts:
1. **ARP Spoofing**: This part of the script sends fake ARP (Address Resolution Protocol) packets on the network to redirect the traffic through the attacker's machine. It allows the attacker to capture network traffic.
2. **DNS Sniffing**: The script listens for DNS queries and logs the domain names being requested.

> **Warning:** Use this script only on networks you own or have permission to analyze. Unauthorized access to network traffic is illegal.

## How It Works
1. **ARP Spoofing**: 
   - The script sends ARP packets to the target machine and the gateway, pretending to be each other.
   - This tricks the target machine into thinking the attacker’s machine is the gateway, redirecting all its traffic to the attacker.

2. **DNS Sniffing**: 
   - It captures DNS requests over the network (UDP port 53).
   - The captured DNS queries and the corresponding source IP addresses are logged and displayed on the terminal.

## Requirements
- **Python 3.x**
- **Scapy**: A powerful Python-based network tool.
- **Root Privileges**: The script requires admin/root access to send ARP packets and sniff network traffic.

### Installing Dependencies:
1. Install Scapy using pip:
   ```bash
   pip install scapy
