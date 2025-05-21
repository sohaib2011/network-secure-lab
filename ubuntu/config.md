This guide will showcase how to configurate an Ubtuntu server as a LAN client for a virutal network environment.


1.The default network adapter is set to NAT, change it to vmnet2 (which is used by pfSense). 

  <img src="https://github.com/user-attachments/assets/669030e9-c584-4147-b7b7-865d368f5077" width=250>




2. The Ubtunu will now communicate with the pfSense and receive an ip adress via DHCP, as shown in the image below.
   <img src=https://github.com/user-attachments/assets/508a4eb0-5563-43e8-b37f-3def9446ea9f width=9000>

3. Other configurations varies by preference. The server is now successfully integrated with the firewall
   
  ![image](https://github.com/user-attachments/assets/7aca8cc0-358d-4007-b8d0-f5976bfaa307)
