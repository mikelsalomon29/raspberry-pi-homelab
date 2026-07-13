\# Tailscale



\## Purpose



Tailscale will be used to securely access the Raspberry Pi from outside the local home network without opening router ports.



This will allow remote SSH access to the Raspberry Pi and access to local homelab services through a private mesh VPN.



\## Planned Setup



\- Device: Raspberry Pi 3 Model B+

\- Remote access method: Tailscale

\- Router port forwarding: not used

\- Primary use: remote SSH access

\- Secondary use: access to homelab dashboards



\## Installation Command



```bash

curl -fsSL https://tailscale.com/install.sh | sh



Authentication Command

sudo tailscale up

Verification Steps



After installation, Tailscale will be verified by:



tailscale status



Remote SSH access will also be tested from another network later.



Notes



Tailscale is preferred over router port forwarding because it reduces exposure to the public internet.

