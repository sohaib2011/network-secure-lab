## Internet connection to DMZ
Before setting up the webserver, we need to establish communication in the traffic between DMZ and WAN. In this case, since the pfsense is the "chief" of routing, we 
should a firewall rule to permit outbound traffic for the DMZ.

In pfsense: 
Add firewall -> Rules -> OPT1 (default name for DMZ), to define rules manually

<img width="700" src="https://github.com/user-attachments/assets/5b35d5b0-3afe-4ca5-a871-cdd5fbdc57ae">

Save and apply changes. DMZ now has WAN access.

Install apache2 sudo apt install apache2-y

<img width="720" height="152" alt="image" src="https://github.com/user-attachments/assets/cac153a7-7f8f-4cbb-971c-7417261f9e2f" />



## Webserver setup


<img width="788" height="647" alt="image" src="https://github.com/user-attachments/assets/3f48e939-ca15-4941-905f-7b6519e674f5" />

