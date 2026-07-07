# Raspberry Pi Homelab

A lightweight self-hosted homelab built on a Raspberry Pi 3 Model B+ to learn Linux server administration, networking, DNS, remote access, Docker, monitoring, and self-hosted services.

## Project Goals

- Build a working home server using low-cost hardware
- Learn Linux administration through SSH
- Configure network-wide DNS filtering with Pi-hole
- Set up secure remote access using Tailscale
- Deploy and manage services with Docker
- Monitor uptime and service health
- Document the full setup for portfolio and GitHub use

## Hardware

- Raspberry Pi 3 Model B+
- 16 GB microSD card
- Micro-USB power supply
- Wi-Fi connection
- Windows laptop for setup and SSH access

## Current Status

| Component | Purpose | Status |
|---|---|---|
| Raspberry Pi OS Lite | Server operating system | Complete |
| SSH | Remote terminal access | Complete |
| Wi-Fi | Network connection | Complete |
| Raspberry Pi Connect | Backup remote access option | Enabled |
| GitHub Repository | Version control and public documentation | Complete |
| Pi-hole | DNS ad/tracker blocking | Complete |
| Tailscale | Secure remote access | Planned |
| Docker | Containerized services | Planned |
| Portainer | Docker management UI | Planned |
| Uptime Kuma | Service monitoring | Planned |

## Skills Demonstrated

- Linux command line
- SSH remote administration
- Raspberry Pi OS setup
- Basic networking
- DNS configuration
- System monitoring
- Technical documentation
- GitHub project organization

## Documentation

- [Hardware](docs/01-hardware.md)
- [Initial Setup](docs/02-initial-setup.md)
- [Networking](docs/03-networking.md)
- [Pi-hole Setup](docs/04-pihole-setup.md)
- [Tailscale](docs/05-tailscale.md)
- [Docker and Portainer](docs/06-docker-portainer.md)
- [Monitoring](docs/07-monitoring.md)
- [Troubleshooting](docs/troubleshooting.md)

## Build Log

See [Build Log](notes/build-log.md).