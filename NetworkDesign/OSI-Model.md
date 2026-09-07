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



# 🌐 Networks & OSI Model — Study Notes

> **CompTIA A+ | 220-1101 Core 1 | Domain 2: Networking**  
> Based on personal study material. Part of my IT Support learning journey.

---

## Table of Contents
- [What is a Network?](#what-is-a-network)
- [Network Types](#network-types)
- [Network Devices](#network-devices)
- [Common Network Services](#common-network-services)
- [The OSI Model — 7 Layers](#the-osi-model--7-layers)
- [A Closer Look at Each Layer](#a-closer-look-at-each-layer)
- [How Data Travels — Encapsulation](#how-data-travels--encapsulation)
- [Why the OSI Model Matters](#why-the-osi-model-matters)

---

## What is a Network?

A **network** connects devices so they can **communicate** and **share resources**.

---

## Network Types

| Abbreviation | Full Name | Scope |
|---|---|---|
| **PAN** | Personal Area Network | Around a single person (e.g., Bluetooth) |
| **LAN** | Local Area Network | Home, office, single building |
| **MAN** | Metropolitan Area Network | City-wide coverage |
| **WAN** | Wide Area Network | Across cities/countries (e.g., the Internet) |

---

## Network Devices

| Category | Examples |
|---|---|
| **End Devices (Hosts)** | PC, laptop, printer, phone, server |
| **Network Devices** | Switch, router, firewall, wireless AP |

### Small Office LAN Layout
```
INTERNET ── ROUTER ── SWITCH ──┬── SERVER
                                ├── PC 1
                                ├── PC 2
                                ├── PRINTER
                                ├── LAPTOP
                                └── WIRELESS AP ── PHONE
```

---

## Common Network Services

- 📁 File sharing
- 🌐 Internet access
- 📧 Email
- 🖨️ Printing
- 🖥️ Remote access
- 📞 VoIP / Video

---

## The OSI Model — 7 Layers

> The **OSI (Open Systems Interconnection)** model is a conceptual framework that standardises how data communicates across a network.

```
┌─────────────────────────────────────────────────┐
│  HIGHER — Closer to User                        │
│                                                  │
│  7 │ APPLICATION   │ Network services to apps   │
│  6 │ PRESENTATION  │ Format, encrypt, compress  │
│  5 │ SESSION       │ Establish & manage sessions│
│  4 │ TRANSPORT     │ End-to-end delivery        │
│  3 │ NETWORK       │ Logical addressing/routing │
│  2 │ DATA LINK     │ Framing, MAC, error detect │
│  1 │ PHYSICAL      │ Raw bits over the medium   │
│                                                  │
│  LOWER — Closer to Hardware                     │
└─────────────────────────────────────────────────┘
```

### 🧠 Mnemonics

| Direction | Mnemonic |
|---|---|
| Top → Bottom (7→1) | **A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing |
| Bottom → Top (1→7) | **P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way |

---

## A Closer Look at Each Layer

### Layer 7 — Application
- Provides network services directly to **user applications**
- Examples: `HTTP`, `FTP`, `SMTP`, `DNS`

### Layer 6 — Presentation
- **Translates, encrypts, and compresses** data
- Examples: `TLS/SSL`, `JPEG`, `ASCII`, `MPEG`

### Layer 5 — Session
- **Manages sessions** between applications (open, maintain, close)
- Examples: `NetBIOS`, `RPC`

### Layer 4 — Transport
- Ensures **end-to-end delivery**, flow control, and error recovery
- Examples: `TCP` (reliable), `UDP` (fast, no guarantee)

| Protocol | Type | Use Case |
|---|---|---|
| **TCP** | Connection-oriented | HTTP, email, file transfer |
| **UDP** | Connectionless | Streaming, VoIP, DNS |

### Layer 3 — Network
- Handles **logical addressing (IP)** and **routing** between networks
- Examples: `IP`, `ICMP`, `OSPF`, `BGP`
- Device: **Router**

### Layer 2 — Data Link
- **Node-to-node delivery**, framing, MAC addressing, error detection
- Examples: `Ethernet`, `Wi-Fi (802.11)`, `PPP`
- Device: **Switch / Bridge**

### Layer 1 — Physical
- Transmits **raw bits** over the physical medium
- Examples: Cables, Fiber, Radio, RJ-45

---

## How Data Travels — Encapsulation

> When data is sent, **each layer adds its own header** (and sometimes trailer).  
> At the destination, **each layer removes its header**.

### Sender (Encapsulation — going DOWN)

```
Application Data
      ↓  + L7 Header
    [ L7 DATA ]
      ↓  + L6/L5 processing
    [ L5 H | L6 H | L7 DATA ]
      ↓  + L4 Header  →  Segment
    [ L4 H | L5 H | L6 H | L7 DATA ]
      ↓  + L3 IP Header  →  Packet
    [ L3 H | L4 H | L5 H | L6 H | L7 DATA ]
      ↓  + L2 MAC Header  →  Frame
    [ L2 H | L3 H | L4 H | L5 H | L6 H | L7 DATA ]
      ↓
    BITS: 0101010001010111001010...
```

### Receiver (De-encapsulation — going UP)
```
Bits → Frame → Packet → Segment → Data
         (headers are stripped at each layer)
```

### Data Unit Names per Layer

| Layer | Data Unit |
|---|---|
| 4 – Transport | **Segment** |
| 3 – Network | **Packet** |
| 2 – Data Link | **Frame** |
| 1 – Physical | **Bit** |

> `H` = Header · `L` = Layer  
> A **Trailer** (e.g., error check) may be added at Layer 2.

---

## Why the OSI Model Matters

- ✅ Provides a **common language** for networking
- ✅ Helps **troubleshoot** — isolate the problem by layer
- ✅ Encourages **standardisation** and interoperability
- ✅ Useful for **learning and designing** networks

### Real-World Device Layers
> You don't always need all 7 layers in real devices.

| Device | Operates At |
|---|---|
| Hub / Cable | Layer 1 |
| Switch / Bridge | Layer 2 |
| Router | Layer 3 |
| Firewall | Layer 3–4 |
| Application Proxy | Layer 7 |

---



## Common Ports (Quick Reference)

| Port | Protocol |
|---|---|
| 80 | HTTP |
| 443 | HTTPS |
| 22 | SSH |
| 21 | FTP |
| 53 | DNS |
| 67/68 | DHCP |
| 25 | SMTP |

---

*Study notes by **Dominion** · IT Support & Networking Journey · [github.com/play86](https://github.com/play86)*
