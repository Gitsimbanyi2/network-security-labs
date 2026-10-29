# network-security-labs

Network defence labs — diagrams, hardening, VLAN, VPN, and troubleshooting.

Lab prefixes: `192.0.2.0/24` (users), `198.51.100.0/24` (servers), `203.0.113.0/24` (simulated untrusted / “internet”). RFC 5737 documentation ranges only.

## Contents

| Path | Topic |
|------|--------|
| `diagrams/lab-network.md` | Mermaid topology |
| `firewall/baseline-hardening.md` | Default-deny, management plane, logging |
| `vlan/segmentation-lab.md` | User / server / management VLANs |
| `vpn/site-to-site-overview.md` | Lab site-to-site intent (no live PSK) |
| `troubleshooting/common-checks.md` | Reachability and policy misses |

No production firewall exports, no real VPN pre-shared keys, no customer subnets.
