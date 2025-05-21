1. Since my Ubuntu Server runs in terminal-mode, and lynx is insufficient for the full access of pfsense interface, we need proper GUI access to pfSense.

The best approach for this would be to access the web interface from host

2. In VMware Workstatin, go to Edit -> Virtual Network Editor

3. Select the internal network pfSense LAN is using, which in my case is vmnet2

4. Make sure the network type is set to host-only and apply the change. This configures the network within VMWare, however we need to configure on the host machine itself.


Control Center Settings and Configurations
1. Gå til kontroll panel -> Nettverk og Internett.
2. Herfra klikk på endre innstillinger for nettverkskort for å endre konfigurasjon i ip-adresse
3. Finn adapteren som heter 'vmware network adapter VMnet2' og høyre-klikk for egenskaper
4. Velg så internet protocol version 4 (TCP/IPv4) og velg egenskaper igjen
5. Heretter endrer du nettverksegenskapene til det ønskelige for ditt miljø.
