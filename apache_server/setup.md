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
