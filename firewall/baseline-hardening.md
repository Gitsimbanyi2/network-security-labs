# Firewall baseline (lab)

## Policy intent

1. Default **deny** inbound from `203.0.113.0/24`.
2. Allow established/related out from users and servers.
3. SSH (22) to servers: source `192.0.2.200` only.
4. Wazuh agent 1514/tcp: servers → `198.51.100.10`.
5. HTTPS 443 to `198.51.100.30` only if the web lab is in scope.
6. Management UI of the firewall: jump host only, not the user VLAN.
7. Log allows and denies to the SIEM lab (UDP/TCP 514 to `198.51.100.10` if you enable syslog — lab).

## Hardening checklist

- [ ] No any/any rule
- [ ] Unused WAN NAT objects removed
- [ ] Admin MFA or at least a unique lab admin account (not `admin`/`password`)
- [ ] Firmware noted in the lab change log
- [ ] Backup of lab config stored offline, **not** in Git

Replace vendor CLI with your lab platform (Sophos, nftables, etc.). Do not commit a dumped production `ossec.conf` or firewall XML.
