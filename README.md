# Packet Tracer Lab: Configure DHCP on a Wireless Router

## Overview

This project demonstrates how to configure Dynamic Host Configuration Protocol (DHCP) on a wireless router using Cisco Packet Tracer. Three PCs are connected to the router and configured to obtain their IP addresses automatically.

The lab focuses on router configuration, IPv4 addressing, DHCP address allocation, and network connectivity verification.

## Objectives

- Connect three PCs to a wireless router using Ethernet cables.
- Inspect the default DHCP configuration.
- Change the router's IP address.
- Configure a custom DHCP address range.
- Configure client devices to obtain IP addresses automatically.
- Verify connectivity using `ipconfig` and `ping`.

## Tools Used

- Cisco Packet Tracer
- Wireless router
- Three generic PCs
- Copper straight-through Ethernet cables
- Command Prompt

## Network Configuration

| Parameter | Configuration |
|---|---|
| Router IP address | `192.168.5.1` |
| DHCP starting IP address | `192.168.5.126` |
| Maximum number of DHCP clients | `75` |
| Client IP configuration | DHCP (automatic) |

## Lab Implementation

### 1. Set Up the Network Topology

- Added three generic PCs and a wireless router.
- Connected each PC to an Ethernet port on the router using copper straight-through cables.
- Waited for the network connections to become active.

### 2. Inspect Default DHCP Settings

- Opened the IP Configuration utility on PC0.
- Selected DHCP to obtain network configuration automatically.
- Recorded the default gateway.
- Accessed the router's web-based configuration page to inspect the default DHCP settings.

### 3. Change the Router IP Address

- Changed the router's IP address to `192.168.5.1`.
- Saved the configuration.
- Renewed PC0's network configuration by switching from Static to DHCP.
- Reconnected to the router's configuration page using its new IP address.

### 4. Configure the DHCP Address Range

- Changed the DHCP starting IP address to `192.168.5.126`.
- Set the maximum number of DHCP clients to `75`.
- Saved the settings.
- Renewed the client IP configuration.

### 5. Configure DHCP on All PCs

- Enabled DHCP on PC0, PC1, and PC2.
- Checked the assigned IP addresses using the IP Configuration utility and the `ipconfig` command.

### 6. Verify Network Connectivity

Used the following commands from PC2:

```text
ipconfig
ping 192.168.5.1
ping 192.168.5.127
```

- `ipconfig` displays the client's IP configuration.
- `ping 192.168.5.1` tests connectivity to the router.
- `ping 192.168.5.127` tests connectivity to the specified client address, provided that PC1 has been assigned that address.

## Results

The wireless router was reconfigured with the IP address 192.168.5.1, and its DHCP starting address was changed to 192.168.5.126.

PC0 received the IP address 192.168.5.126, and PC1 received 192.168.5.127. The clients were configured to obtain IP addresses automatically using DHCP.

Connectivity was tested using ipconfig and ping commands to check network configuration and communication between devices.

## Key Learnings

- Understanding DHCP and automatic IP address allocation.
- Configuring a router's LAN IP address.
- Understanding DHCP address pools and client limits.
- Identifying a default gateway.
- Using `ipconfig` to inspect network settings.
- Using `ping` to test network connectivity.
- Troubleshooting basic network configuration issues.

## Cybersecurity Relevance

DHCP and IP addressing are important foundations for network security and troubleshooting. Understanding how devices receive network configurations helps analysts identify unexpected addressing, investigate connectivity issues, and understand communication between devices on a local network.


Recommended screenshots:

1. Network topology showing all three PCs connected to the router.
2. Router configuration showing the IP address and DHCP settings.
3. `ipconfig` output from the client PCs.
4. Successful ping output to the router.
5. Successful ping output to PC1, if verified.

## Conclusion

This lab provided practical experience configuring DHCP on a wireless router, assigning IP addresses automatically, and testing communication between network devices in a simulated environment.

**Environment:** Cisco Packet Tracer  
**Project Type:** Networking Fundamentals / Cybersecurity Lab Portfolio
