\# Initial Setup



\## Operating System



The Raspberry Pi was flashed with Raspberry Pi OS Lite 32-bit using Raspberry Pi Imager.



\## Raspberry Pi Imager Configuration



The following settings were configured before writing the microSD card:



\- Device: Raspberry Pi 3

\- Operating System: Raspberry Pi OS Lite 32-bit

\- Hostname: `pihomelab`

\- SSH: enabled

\- Wi-Fi: configured

\- Raspberry Pi Connect: enabled

\- User account: configured

\- Localization: configured



\## First Boot



After flashing the microSD card, it was inserted into the Raspberry Pi and powered using a micro-USB power cable.



The Pi was given several minutes to boot, connect to Wi-Fi, and become available on the local network.



\## SSH Connection



The Raspberry Pi was accessed from Windows PowerShell using SSH:



```powershell

ssh mikel@pihomelab.local



On the first connection, the SSH fingerprint warning appeared and was accepted.



\## System Update



After logging in, the system package list was updated and installed packages were upgraded:



sudo apt update

sudo apt full-upgrade -y

sudo reboot

System Verification



After rebooting, the following commands were used to verify the system:



hostname

df -h

free -h

vcgencmd measure\_temp

Results

Hostname confirmed as pihomelab

Storage: 14 GB total, 2.6 GB used, 11 GB available

Memory: 920 MiB total, 706 MiB free

Temperature: 42.9°C

SSH access from Windows confirmed working

Notes



The Raspberry Pi 3 Model B+ micro-USB port is used for power, not direct data access to the Windows laptop. Headless access was completed over Wi-Fi using SSH.

