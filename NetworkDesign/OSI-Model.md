# 🌐 Networks & The OSI Model

<details>
<summary>📖 <b>Networks Overview</b></summary>
<br>

- **Types:** PAN · LAN · MAN · WAN
- **LAN devices:** Router, Switch, Server, AP, PC, Printer, Laptop, Phone
- **Hosts** (end devices) vs **Network devices** (switches, routers, firewalls)
- **Services:** File sharing · Internet · Email · Printing · Remote access · VoIP/Video

</details>

<details>
<summary>🧩 <b>OSI Model — 7 Layers</b></summary>
<br>

| # | Layer |
|:-:|---|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |

**Higher** = closer to user · **Lower** = closer to hardware

</details>

<details>
<summary>🔍 <b>Layer Protocols</b></summary>
<br>

| Layer | Protocols |
|---|---|
| Application | HTTP, FTP |
| Presentation/Session | TLS/SSL |
| Transport | TCP, UDP |
| Network | IP, OSPF |
| Data Link | Ethernet/MAC, PPP |
| Physical | Fiber, Radio |

</details>

<details>
<summary>📦 <b>Encapsulation</b></summary>
<br>

- **↓ Sender:** headers added at each layer
- **↑ Receiver:** headers stripped at each layer
- Physical layer = raw **bits**

</details>

<details>
<summary>❓ <b>Why OSI Matters</b></summary>
<br>

- Common language for networking
- Troubleshoot layer by layer (L7 → L1)
- Standardization & interoperability

> ⚠️ Switches = L1–L2 · Routers = L3

</details>

<p align="center">
  <img width="700" alt="Network-OSI_OVERVIEW" src="https://github.com/user-attachments/assets/a32630de-a953-4a21-a33a-0079341f5c3d">
</p>
