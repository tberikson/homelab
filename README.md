# Homelab

## Description
This GitHub repository serves as a public-facing collection of documentation pertaining to personal technical projects. Topics (will) include:
* Linux,
* automation,
* networking,
* monitoring,
* Home Assistant,
* Large Language Models (LLMs),
* troubleshooting,
* 3D printing (FDM).

## Desktop
Primary workstation for daily computing running Arch Linux with KDE Plasma desktop and Wayland compositor; mobile workstation (laptop) doubling as a media center running a similar configuration, with additional power management utilities (MSI-specific EC for battery charge limiting), and a different firewall front-end (firewalld instead of ufw).

## Media Server
Media server running Debian Linux. It provides a variety of services for the household, such as OpenWebUI, Jellyfin, AI text-to-speech, and other GPU workloads as needed.

## Home Assistant
Raspberry Pi SBC running Home Assistant. It primarily serves as a remote method to control the state of the primary workstation. For example, send magic packets to Wake-on-Lan, reboot/shutdown over SSH, etc. using mobile phone widgets. Functionality has been added to control certain network-enabled lights. It also had Waze integrated to estimate commute times to the workplace, sent via push notification at predefined times. More functionality is planned to be added later.
