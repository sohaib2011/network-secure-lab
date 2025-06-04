This guide is a walkthrough for setting up a webserver inside a DMZ

### Network Adapter Configuration

1. Add a new network adapter as shown in the /pfSense folder in github. This will be connected to VMnet3. The same process must ...

2. Now, on pfSense VM, assign the new interface by selecting the option  1) Assign a new interface in the terminal:

   ![image](https://github.com/user-attachments/assets/3a84be8e-71bb-4440-b337-93e3fd413e8e)

3. Our DMZ interface is now added under the name of 'OPT1' 

   ![image](https://github.com/user-attachments/assets/cba20c8f-d9b7-4830-9a87-63b4de6ca0e1)

4. For extra confirmation, we can see through the GUI that the new interface has been recognized:

   <img src=https://github.com/user-attachments/assets/7f5cf885-7192-46de-bf87-37b7b1f6dba3 width=700>

5. Finally, we enable the interface to allow netweork communicatoin for the dmz:

   ![image](https://github.com/user-attachments/assets/b62cfb66-0d49-43ec-b13d-8675d4c954d5)

 
### Ubuntu Network Adapter Configuration
The LAN client cant share the same network interface as the dmz webserver. The simplesst appproach is to clone the existing Ubuntu VM and chcange its network adapter to VMnet3

 1. ens33 (the adapter connected to VMnet) is not assigned to any ip adresses. Since this server will act as the webserver in DMZ, we must assign a static ip adress. Assignment through DHCP would be unideal and a bad choice for tihs

     ![image](https://github.com/user-attachments/assets/e5d596f7-d638-4968-ab99-85cfe2c5c564)

 2. Netplan is responsible for the network config for the server, hence we need to locate its respective .yaml file.

     ![image](https://github.com/user-attachments/assets/eee16e82-fb3f-44e6-9876-55b2e45fd6b1)

     ![image](https://github.com/user-attachments/assets/93c7bf06-983b-49c9-815f-13f71b028a7e)

 3. Run 'sudo netplan apply' to read and confirm the changes made in the .yaml file
    
    ![image](https://github.com/user-attachments/assets/ef4007ea-05c2-478b-9537-91d2d177796d)
 
4. For the host access, the same steps applies here as in /pfsense/host-access-to-vms.md. However for this VM, change uncheck "Use local dhcp to distribute ip adress to vms" in Virtual Network Editor.
   The reason for this is because we are using static ips.
