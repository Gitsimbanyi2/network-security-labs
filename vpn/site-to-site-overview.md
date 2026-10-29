# Site-to-site VPN — lab overview

Two imaginary sites:

| Site | LAN | Tunnel overlay |
|------|-----|----------------|
| Site A | 192.0.2.0/24 | 172.16.0.1 (lab only) |
| Site B | 198.51.100.0/24 | 172.16.0.2 (lab only) |

## What to document in a real change (do not put secrets here)

- Encryption: AES-256, SHA-256, DH group 14 or better
- Dead peer detection on
- Interesting traffic: the two lab prefixes only
- PSK or certificate — store in the enterprise vault, **never** in Git

This file is the design note. It is not a working config with a key.
