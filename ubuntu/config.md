This guide will showcase how to configure an Ubuntu Server as a LAN client in a virtual network environment using pfSense as the firewall and DHCP server.

---

### 1. Change Network Adapter to VMnet2

The default network adapter is set to NAT. Change it to VMnet2, which is used by pfsense.

<img src="https://github.com/user-attachments/assets/669030e9-c584-4147-b7b7-865d368f5077" width="400">

---

### 2. Verify DHCP Connection to pfSense

The Ubtunu will now communicate with the pfSense and automatically receive an ip adress via DHCP, as shown in the image below.

<img src="https://github.com/user-attachments/assets/508a4eb0-5563-43e8-b37f-3def9446ea9f" width="600">

---

### 3. Complete the Installation

Other configurations varies by preference in the following steps, however i just skipped through. The server is now successfully integrated with the firewall

<img src="https://github.com/user-attachments/assets/7aca8cc0-358d-4007-b8d0-f5976bfaa307" width="400">

---

### 4. Test Network Connectivity

To ensure that the connection works, i will proceed a random ping

   ![image](https://github.com/user-attachments/assets/c4283b37-7f4b-4939-a063-888064baf09e)
