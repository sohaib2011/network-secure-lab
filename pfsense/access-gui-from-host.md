### VMware Configurations 

1. Since my Ubuntu Server runs in terminal-mode, and lynx is insufficient for the full access of pfsense interface, we need proper GUI access to pfSense.

   The best approach for this would be to access the web interface from host.

2. In VMware Workstatin, go to Edit -> Virtual Network Editor.

3. Select the internal network pfSense LAN is using, which in my case is vmnet2.

4. Make sure the network type is set to host-only and apply the change. This configures the network within VMWare, however we need to configure on the host machine itself.

---

### Control Center Settings and Configurations

1. Gå til kontroll panel -> Nettverk og Internett.

2. Herfra klikk på endre innstillinger for nettverkskort for å endre konfigurasjon i ip-adresse.

3. Finn adapteren som heter 'vmware network adapter VMnet2' og høyre-klikk for egenskaper.

  <img src="https://github.com/user-attachments/assets/528f675d-686b-4010-bdbd-416dd7a992b5" width=350>


5. Velg så internet protocol version 4 (TCP/IPv4) og velg egenskaper igjen.

6. Heretter endrer du nettverksegenskapene til det ønskelige for ditt miljø. Foretrukket DNS-server er satt opp til å bli 8.8.8.8 fordi google=konge

   <img src=https://github.com/user-attachments/assets/91103618-d366-473a-bad4-65fbf359f36f width=350>





Result:

   <img src=https://github.com/user-attachments/assets/2dfa5818-3f61-4aec-a596-3873aa0371df width=600>
