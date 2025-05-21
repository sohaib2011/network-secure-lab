## pfSense Configuration in Virtual Lab Environment

This guide documents the configuration of pfSense in a virtual lab environment. Installasjon er tatt til siden og ikke vurdert som del av prosess

---

### 1. Network Setup in VMWare

pfSense requires at least two network adapters:

- WAN: Connected to NAT, which provides internet access  
- LAN: Connected to an internal communication

1. Open **VM Settings** → Click **Add** and choose **Network Adapter**. This creates a new adapter.

2. New adapter: Change network connection to **Custom** → Select **VMnet2** or any other internal network.

   ![image](https://github.com/user-attachments/assets/3b6f1193-ea94-4edf-8405-ed3bfffba5ac)

3. Start VM 👹

---

### 2. pfSense Interface Configuration

1. As showcased in the image below, both network adapters are successfully recognized by pfSense.

   vmware assigns adapters in order, so with this in mind we can assume em0 is NAT.

   An identical GUI will appear for LAN, we proceed by assigning the remaining adapter which is em1.

   <img src="https://github.com/user-attachments/assets/de7ea183-0178-4898-92a3-bb9712d5b5e9" width=500>

2. Likewise for LAN, we will assign the remaining adapter which is em1.

   As a result we have now been successfully given a static ip within a /24 CIDR subnet. DHCP will then assign dynamic ip adresses to clients between 192.168.1.100 to x.x.x.150

   <img src="https://github.com/user-attachments/assets/84124ca1-f367-4252-8006-13b598cdbf92" width=500>

3. Skip the remaining prompts, and your done!

   Note: I chose not to include it since its not relevant for a guide.
   
   ![image](https://github.com/user-attachments/assets/7665f32e-3c2d-4bf7-b178-eae4334b905e)

