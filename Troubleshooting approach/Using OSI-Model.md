
## OSI Troubleshooting Cheat Sheet

| Layer | Abbr | Question to Ask |
|---|---|---|
| 7 – Application | APP | Can the application connect? |
| 6 – Presentation | PRES | Is data in the right format? |
| 5 – Session | SESS | Is the session established? |
| 4 – Transport | TRANS | Is data getting through end-to-end? |
| 3 – Network | NET | Is there a routing path? |
| 2 – Data Link | DL | Are frames being delivered locally? |
| 1 – Physical | PHY | Is the cable/link working? |

---
## Common Ports — Grouped by Use Case

### 🌐 Web & Remote Access

**TCP**

| Port | Protocol | Description |
|---|---|---|
| 80 | HTTP | Unencrypted web traffic |
| 443 | HTTPS | Encrypted web traffic (TLS/SSL) |
| 8080 | HTTP-alt | Alternative / dev web server port |
| 8443 | HTTPS-alt | Alternative HTTPS (often used by apps) |
| 22 | SSH | Secure remote shell / file transfer (SFTP) |
| 23 | Telnet | Unencrypted remote access ⚠️ legacy |
| 3389 | RDP | Windows Remote Desktop Protocol |
| 5900 | VNC | Remote desktop (Virtual Network Computing) |
| 21 | FTP | File transfer — control channel |
| 20 | FTP-data | File transfer — data channel |

### 📧 Mail Cluster

**TCP**

| Port | Protocol | Description |
|---|---|---|
| 25 | SMTP | Server-to-server email sending |
| 587 | SMTP (TLS) | Client email submission (authenticated) |
| 465 | SMTPS | SMTP over SSL (legacy, still used) |
| 110 | POP3 | Retrieve email — deletes from server |
| 995 | POP3S | POP3 over SSL/TLS |
| 143 | IMAP | Retrieve email — keeps on server |
| 993 | IMAPS | IMAP over SSL/TLS |

### 🔧 Quiet Infrastructure (Background Services)

**TCP**

| Port | Protocol | Description |
|---|---|---|
| 179 | BGP | Border Gateway Protocol — internet routing |
| 389 | LDAP | Directory services (Active Directory) |
| 636 | LDAPS | LDAP over SSL — secure directory lookup |

**UDP**

| Port | Protocol | Description |
|---|---|---|
| 53 | DNS | Domain name resolution |
| 67 | DHCP (server) | Server assigns IP addresses to clients |
| 68 | DHCP (client) | Client receives IP address from server |
| 123 | NTP | Network Time Protocol — clock sync |
| 161 | SNMP | Network device monitoring (queries) |
| 162 | SNMP Trap | Network device alerts (notifications) |
| 514 | Syslog | System log forwarding to log server |

**TCP / UDP**

| Port | Protocol | Description |
|---|---|---|
| 53 | DNS | Falls back to TCP for large responses (zone transfers) |
| 389 | LDAP | Can run over either; TCP preferred for reliability |

---
