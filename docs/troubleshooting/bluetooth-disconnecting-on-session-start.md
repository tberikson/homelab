Problem:
Bluetooth disconnects/refuses to connect devices on user session start.

Symptoms:
Logging in disconnects Bluetooth devices and refuses to reconnect them.

Investigation:
- Checked Realtek adapter power settings
- Experimented with Bluetooth daemon
- Examined journalctl

Root Cause:
Bluetooth adapter itself was unstable due to the ASUS/Realtek autosuspend policy. Bluetooth would start normally at boot, but during the login process the Bluetooth service is re-initialized but in a broken state.

Resolution:
Workarounds involved installing a persistent udev rule for ASUS/Realtek power policy and adding a delayed user-side timer that restarts bluetooth.service after login has settled.
