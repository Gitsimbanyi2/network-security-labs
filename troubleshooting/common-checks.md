# Troubleshooting (lab)

| Symptom | First checks |
|---------|----------------|
| Agent disconnected | Ping `198.51.100.10` from agent; `ss -lntp` for 1514 on manager; firewall allow list |
| Users reach server SSH | Policy leak VLAN 10 → 22; remove it |
| VPN up, no routes | Interesting traffic / NAT-T / phase 2 selectors |
| Deny log flood from 203.0.113.88 | Expected if the scanner lab is on; do not “allow to stop the noise” |

Commands (Linux lab host):

```bash
ip -br a
ip route
ss -lntp
sudo nft list ruleset | head
ping -c 3 198.51.100.10
```
