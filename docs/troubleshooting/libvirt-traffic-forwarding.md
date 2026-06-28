Problem:
QEMU guest VM cannot reach outside network.

Symptoms:
Performing network operations within VM like ping or curl result in failure, "network is unreachable."

Investigation:
- Examined virtual network configuration and status
- Checked firewall rules

Root Cause:
Host firewall was denying forwarding packets.

Resolution:
Changed host firewall configuration to allow forwarding packets.