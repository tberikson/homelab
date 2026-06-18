# Homelab

## Description
This GitHub repository serves as a public-facing collection of documentation pertaining to my personal technical projects. Topics (will) include:
* Linux,
* automation,
* networking,
* monitoring,
* Home Assistant,
* Large Language Models (LLMs),
* troubleshooting,
* 3D printing (FDM).

## Desktop
My main personal computer is running Arch Linux with the KDE Plasma desktop and Wayland compositor; my laptop is running pretty much the same configuration, with the addition of some power management utilities (MSI-specific EC for battery charge limiting), and a different firewall.

## Media Server
Our media server is running Debian Linux. It runs a variety of services, such as OpenWebUI, Jellyfin, AI text-to-speech, and whatever else needs GPU compute we don't want running on our own machines.

## Home Assistant
I have a Raspberry Pi SBC running Home Assistant. It primarily serves as a remote way to send commands to my machine. For example, I can wake-on-lan, reboot, or shutdown my PC by just tapping a widget on my phone. It controls my bedroom light and has a Waze automation that provides me with a commute time estimate at a set time every day for my workplace. I plan to add more functionality later.
