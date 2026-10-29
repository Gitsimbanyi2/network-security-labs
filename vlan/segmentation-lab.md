# VLAN segmentation lab

| VLAN | Name | Prefix | Who |
|------|------|--------|-----|
| 10 | Users | 192.0.2.0/24 | Analyst workstation |
| 20 | Servers | 198.51.100.0/24 | Wazuh, web lab |
| 99 | Management | 192.0.2.192/26 | Jump host, firewall admin |

## Rules of the exercise

- User VLAN cannot SSH to servers.
- Management VLAN can SSH and reach HTTPS admin.
- Servers cannot initiate to the user VLAN except return traffic.
- No VLAN hopping tests against production switches — this write-up is the lab.

## Why it matters

A workstation malware infection should not reach the SIEM manager’s SSH port. That is the same idea used in a SACCO/CBS estate, demonstrated here with documentation IPs only.
