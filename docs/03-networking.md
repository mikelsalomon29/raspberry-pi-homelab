\# Networking



\## Current Network Setup



The Raspberry Pi is connected to the local network over Wi-Fi.



\- Hostname: `pihomelab`

\- Network interface: `wlan0`

\- Current IPv4 address: `192.168.1.246`

\- Access method: SSH from Windows PowerShell

\- Pi-hole dashboard: `http://192.168.1.246/admin`



\## SSH Access



The Raspberry Pi can be accessed from the Windows laptop using:



```powershell

ssh mikel@pihomelab.local



DNS Testing



Pi-hole was first tested only on the Windows laptop instead of the entire router.



The Windows laptop was manually configured to use the Raspberry Pi as its DNS server:



Preferred DNS: 192.168.1.246



This confirmed that Pi-hole worked without affecting the rest of the home network.



Current Decision



Router-wide DNS has not been enabled yet. Pi-hole is currently being tested on a single Windows laptop to avoid disrupting other devices on the network.



Next Networking Step



Reserve a stable IP address for the Raspberry Pi in the router settings so the Pi-hole DNS address does not change.

