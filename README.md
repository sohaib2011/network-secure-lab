## Objective


## Network Architecture

This lab replicates a simplified enterprise network environment using **pfSense** as the core router/firewall

- **WAN (Wide Area Network):**
  - Connected to VMware1 (NAT)
  - Provides outbound internet access to the environment

- **LAN (Local Area Network):**
  - Connected to VMnet2, and represents the internal network where trusted hosts can operate
  - DHCP is handled by pfSense to assign IPs within the LAN subnet
    
- **DMZ (Demilitarized Zone):** 
  - This network will host services exposed to NAT (e.g Apache webserver) in a seperated, isolated subnet to reduce risk to the internal LAN
  - Allows inbound traffic from WAN, but blocks all outgoing from DMZ to LAN
  
---


<!--
### 🏢 Purpose of Design

This structure emulates a **real-world enterprise network** where:

- **pfSense** acts as the central **security perimeter** and **routing device**
- **LAN** contains internal resources (such as servers, endpoints, or domain controllers)
- **WAN** simulates internet connectivity
- **DMZ** will serve as an isolated buffer zone for systems that need limited external access (e.g., HTTP/S or SSH from WAN)
-->
