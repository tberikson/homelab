# Migrating from KDE Plasma to Hyprland on Arch Linux

## Goal

Experiment with a compositor-centric workflow and better understand how a modern Linux desktop session is assembled.

## Initial Observations

Hyprland itself was straightforward to install and launch. Plasma Login Manager (KDE's fork of SDDM) automatically detected Hyprland, though it can also be launched from a tty using start-hyprland. Most of the work involved recreating services that Plasma previously provided automatically.

## Problems Encountered

### Secret Service Integration

Applications that required a secret manager to function properly, like Vivaldi, requested to open KDE Wallet on launch, which was undesirable. KDE Wallet needed to be unlocked on login.

This led to investigating:

* KWallet
* Freedesktop Secret Service
* Session services
* D-Bus integration

### Theming

GTK and Qt applications required separate configuration.

Topics:

* qt6ct
* Kvantum
* GTK themes
* Environment variables

### Fonts and Icons

Some UI glyphs rendered as missing-character boxes in ashell. Resolution involved configuring applications to use specific fonts.

### Power Management

Plasma normally handles:

* Screen locking
* Idle behavior
* Suspend integration

The services needed to be installed and configured separately in Hyprland.

### Window Rules

Hyprland provides robust window management. Typical applications automatically open on preferred monitors (workspaces), and each is configured to use a different layout scheme.

Examples:

* Vivaldi -> right monitor
* Thunderbird -> left monitor
* Steam -> center monitor

### Lessons Learned

A desktop environment is much more than a compositor.

Plasma automatically provides:

* Secret storage
* Session management
* Power management
* Notifications
* Portals
* Theming integration

Building a Hyprland environment from scratch exposed these services individually and helped improve understanding of how the Linux desktop stack is assembled.

## Current Status

Functional daily-driver configuration with ongoing experimentation around layouts and workflows.