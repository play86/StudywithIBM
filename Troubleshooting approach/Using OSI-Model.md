
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

## Common Ports — Grouped by Use Case
 
| Port | Protocol | TCP | UDP | Use Case | Description |
|---|---|:---:|:---:|---|---|
| 20 | FTP-data | ✅ | | 🌐 Web & Remote | File transfer — data channel |
| 21 | FTP | ✅ | | 🌐 Web & Remote | File transfer — control channel |
| 22 | SSH | ✅ | | 🌐 Web & Remote | Secure remote shell / file transfer (SFTP) |
| 23 | Telnet | ✅ | | 🌐 Web & Remote | Unencrypted remote access ⚠️ legacy |
| 25 | SMTP | ✅ | | 📧 Mail | Server-to-server email sending |
| 53 | DNS | ✅ | ✅ | 🔧 Infrastructure | Name resolution; TCP for zone transfers |
| 67 | DHCP (server) | | ✅ | 🔧 Infrastructure | Server assigns IP addresses to clients |
| 68 | DHCP (client) | | ✅ | 🔧 Infrastructure | Client receives IP address from server |
| 80 | HTTP | ✅ | | 🌐 Web & Remote | Unencrypted web traffic |
| 110 | POP3 | ✅ | | 📧 Mail | Retrieve email — deletes from server |
| 123 | NTP | | ✅ | 🔧 Infrastructure | Network Time Protocol — clock sync |
| 143 | IMAP | ✅ | | 📧 Mail | Retrieve email — keeps on server |
| 161 | SNMP | | ✅ | 🔧 Infrastructure | Network device monitoring (queries) |
| 162 | SNMP Trap | | ✅ | 🔧 Infrastructure | Network device alerts (notifications) |
| 179 | BGP | ✅ | | 🔧 Infrastructure | Border Gateway Protocol — internet routing |
| 389 | LDAP | ✅ | ✅ | 🔧 Infrastructure | Directory services (Active Directory) |
| 443 | HTTPS | ✅ | | 🌐 Web & Remote | Encrypted web traffic (TLS/SSL) |
| 465 | SMTPS | ✅ | | 📧 Mail | SMTP over SSL (legacy, still used) |
| 514 | Syslog | | ✅ | 🔧 Infrastructure | System log forwarding to log server |
| 587 | SMTP (TLS) | ✅ | | 📧 Mail | Client email submission (authenticated) |
| 636 | LDAPS | ✅ | | 🔧 Infrastructure | LDAP over SSL — secure directory lookup |
| 993 | IMAPS | ✅ | | 📧 Mail | IMAP over SSL/TLS |
| 995 | POP3S | ✅ | | 📧 Mail | POP3 over SSL/TLS |
| 3389 | RDP | ✅ | | 🌐 Web & Remote | Windows Remote Desktop Protocol |
| 5900 | VNC | ✅ | | 🌐 Web & Remote | Remote desktop (Virtual Network Computing) |
| 8080 | HTTP-alt | ✅ | | 🌐 Web & Remote | Alternative / dev web server port |
| 8443 | HTTPS-alt | ✅ | | 🌐 Web & Remote | Alternative HTTPS (often used by apps) |
 
---
---
