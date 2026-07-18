# Build Log

## Day 1 - Initial Raspberry Pi Setup

### Goal

Set up a Raspberry Pi 3 Model B+ as the base for a lightweight homelab.

### Hardware Used

- Raspberry Pi 3 Model B+
- 16 GB microSD card
- Micro-USB power cable
- Windows laptop
- Wi-Fi network

### Operating System

- Raspberry Pi OS Lite 32-bit

### Configuration Applied in Raspberry Pi Imager

- Hostname: pihomelab
- Username: mikel
- SSH: enabled
- Wi-Fi: configured
- Raspberry Pi Connect: enabled
- Localization: configured

### Commands Run

```bash
sudo apt update
sudo apt full-upgrade -y
sudo reboot

###
Completed:
- Flashed Raspberry Pi OS Lite 32-bit
- Enabled SSH
- Configured Wi-Fi
- Enabled Raspberry Pi Connect
- Booted Raspberry Pi 3 Model B+
- Connected from Windows PowerShell over SSH
- Updated system packages
- Verified hostname, storage, RAM, and temperature


## Milestone - Pi-hole Working on Laptop

### Goal

Install and test Pi-hole as the first real homelab service.

### What Was Completed

- Installed Pi-hole on the Raspberry Pi 3 Model B+
- Selected `wlan0` as the network interface
- Used Cloudflare (DNSSEC) as the upstream DNS provider
- Enabled the web admin dashboard
- Enabled query logging
- Set FTL privacy mode to show everything for learning and troubleshooting
- Logged into the Pi-hole dashboard
- Rebuilt the gravity database using `pihole -g`
- Configured the Windows laptop to use Pi-hole as its DNS server
- Tested normal browsing for about one week

### Result

Pi-hole is working successfully on the Windows laptop without major browsing or network issues.

### Current Decision

Pi-hole is not being applied router-wide yet. The Raspberry Pi will continue to provide DNS filtering only for the Windows laptop for now.



## Tailscale Remote Access

Tailscale is installed on the Raspberry Pi and Windows laptop.

It creates a secure private network between the devices, allowing the Raspberry Pi to be accessed remotely without opening ports on the router.

SSH connection:

```bash
ssh mikel@pihomelab

