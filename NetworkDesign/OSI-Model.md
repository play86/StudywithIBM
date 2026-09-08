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
- [OSI Troubleshooting Cheat Sheet](#osi-troubleshooting-cheat-sheet)
- [Common Ports — Grouped by Use Case](#common-ports--grouped-by-use-case)

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
