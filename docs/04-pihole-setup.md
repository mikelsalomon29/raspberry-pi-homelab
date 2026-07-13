\# Pi-hole Setup



\## Purpose



Pi-hole will be used as a DNS-based ad and tracker blocker for devices on the local network.



For this homelab, Pi-hole is the first real service because it is lightweight, useful, and teaches DNS fundamentals.



\## Planned Setup



\- Device: Raspberry Pi 3 Model B+

\- Interface: `wlan0`

\- Admin interface: enabled

\- Query logging: enabled

\- Initial testing: Windows laptop only

\- Router-wide DNS: later, after testing



\## Installation Command



```bash

curl -sSL https://install.pi-hole.net | bash


\## Configuration Choices



\- Network interface: `wlan0`

\- Upstream DNS provider: Cloudflare (DNSSEC)

\- Blocklist: StevenBlack's Unified Hosts List

\- Web admin interface: enabled

\- Web server: enabled

\- Query logging: enabled

\- Privacy mode: Show everything



\## Verification Results



Pi-hole was verified with:



```bash

pihole status

hostname -I

FTL is listening on port 53

UDP IPv4 enabled

TCP IPv4 enabled

UDP IPv6 enabled

TCP IPv6 enabled

Pi-hole blocking is enabled

Raspberry Pi IPv4 address: 192.168.1.246

Pi-hole dashboard opened successfully in browser

Admin password was reset using pihole setpassword





\## Gravity Database Fix



After the initial dashboard loaded, the "Domains on Lists" card showed:



```text

Error (-2)



This was fixed by rebuilding the Pi-hole gravity database 

&#x09;pihole -g



After rebuilding gravity, the dashboard showed:



Domains on Lists: 78,188

Pi-hole status: Active

Blocking confirmed working

## One-Week Laptop DNS Test

Pi-hole was tested on the Windows laptop before making any router-wide DNS changes.

Test setup:

- Device using Pi-hole DNS: Windows laptop
- DNS server: `192.168.1.246`
- Test length: approximately one week
- Router-wide DNS: not enabled

Results:

- Normal browsing worked
- Google, YouTube, GitHub, and UF websites loaded normally
- Pi-hole dashboard showed active DNS queries from the laptop
- No major network issues were observed during the test

Decision:

Router-wide DNS changes were postponed. Pi-hole will continue to be used on the Windows laptop only for now.



