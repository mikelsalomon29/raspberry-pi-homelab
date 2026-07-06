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