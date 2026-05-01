<div align="center">
 
# 🔍 YourPortScanner
 
### `[ REAL-TIME NETWORK PORT INTELLIGENCE TOOL ]`

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.1.3-black?style=for-the-badge&logo=flask&logoColor=white)
![Security](https://img.shields.io/badge/Security-Tool-red?style=for-the-badge&logo=hackthebox&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

<div align="center">

```
┌─────────────────────────────────────────────────────────────┐
│  TARGET ACQUIRED  >>>  SCANNING PORTS  >>>  RISK ANALYSIS   │
└─────────────────────────────────────────────────────────────┘
```

**Python Project by V.Mouli**

</div>

---

## `> ABOUT`

**YourPortScanner** is a web-based port scanning tool that streams results live to your browser using Server-Sent Events (SSE). It features a cyberpunk-inspired UI with real-time results, a built-in port intelligence database, and risk analysis for every discovered open port — from service identification to known CVE warnings.

---

## `> FEATURES`

```
[+] Real-Time Scanning     — Results stream live via Server-Sent Events (SSE)
[+] Multi-Threaded Engine  — Up to 200 concurrent threads for speed
[+] Risk Intelligence      — Built-in DB with 50+ ports and risk metadata
[+] Flexible Port Modes    — Scan specific ports or full range (1–65535)
[+] Cyberpunk Web UI       — Neon-lit grid interface with scanline overlay
[+] Hostname Resolution    — Accepts both IP addresses and domain names
[+] Risk Classification    — LOW / MEDIUM / HIGH / CRITICAL risk levels
```

---

## `> PROJECT STRUCTURE`

```
YourPortScanner/
├── app.py                  # Core Flask app & multi-threaded scanning engine
├── templates/
│   └── index.html          # Cyberpunk frontend (Tailwind CSS + SSE)
└── venv/                   # Python virtual environment
```

---

## `> TECH STACK`

| Layer | Technology | Version |
|---|---|---|
| Backend | Python + Flask | 3.1.3 |
| Scanning | `socket` + `threading` | stdlib |
| Streaming | Server-Sent Events (SSE) | — |
| Frontend | Tailwind CSS | CDN |
| Fonts | Exo 2, Share Tech Mono, Rajdhani | Google Fonts |

---

## `> DEPENDENCIES`

```
Flask==3.1.3
Werkzeug==3.1.8
Jinja2==3.1.6
click==8.3.3
blinker==1.9.0
itsdangerous==2.2.0
colorama==0.4.6
MarkupSafe==3.0.3
```

---

## `> INSTALLATION`

**Step 1 — Navigate to the project directory**
```bash
cd YourPortScanner
```

**Step 2 — Create virtual environment**
```bash
python -m venv venv
```

**Step 3 — Activate virtual environment**
```bash
# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

**Step 4 — Install Flask**
```bash
pip install flask
```

**Step 5 — Launch the server**
```bash
python app.py
```

**Step 6 — Open in browser**
```
http://127.0.0.1:5000
```

---

## `> HOW TO USE`

```
[1] Enter a target IP or hostname  →  e.g. 192.168.1.1  or  example.com
[2] Choose scan mode               →  Specific Ports  or  All Ports (1-65535)
[3] Enter port list (if specific)  →  e.g. 22,80,443,3306,3389
[4] Hit SCAN                       →  Results stream live to the UI
[5] Analyze results                →  Service name + risk level per open port
```

---

## `> RISK LEVEL MATRIX`

```
┌────────────┬──────────────────────────────────────────────────────────┐
│  CRITICAL  │  Severe risk. Must not be publicly exposed.               │
│            │  → SMB (445), RDP (3389), MySQL (3306), MongoDB (27017)  │
├────────────┼──────────────────────────────────────────────────────────┤
│    HIGH    │  Significant attack surface. Review immediately.          │
│            │  → FTP (21), TFTP (69), NetBIOS (137), VNC (5900)        │
├────────────┼──────────────────────────────────────────────────────────┤
│   MEDIUM   │  Requires attention — potential misuse if misconfigured.  │
│            │  → SSH (22), HTTP (80), SMTP (25), DNS (53)              │
├────────────┼──────────────────────────────────────────────────────────┤
│    LOW     │  Generally safe with proper TLS/auth configuration.       │
│            │  → HTTPS (443), IMAPS (993), POP3S (995)                 │
└────────────┴──────────────────────────────────────────────────────────┘
```

---

## `> PORT INTELLIGENCE DATABASE`

The scanner includes metadata for **50+ well-known ports**, covering:

```
NETWORK      →  21 (FTP), 22 (SSH), 23 (Telnet), 25 (SMTP), 53 (DNS)
WEB          →  80 (HTTP), 443 (HTTPS), 8080 (HTTP Alt), 8443 (HTTPS Alt)
DATABASES    →  1433 (MSSQL), 3306 (MySQL), 5432 (PostgreSQL)
             →  6379 (Redis), 9200 (Elasticsearch), 27017 (MongoDB)
WINDOWS      →  135 (MS RPC), 139 (NetBIOS), 445 (SMB / EternalBlue)
REMOTE ACC.  →  3389 (RDP / BlueKeep), 5900 (VNC), 4444 (Metasploit)
CONTAINERS   →  2375 (Docker HTTP), 2376 (Docker TLS)
```

Unknown ports are auto-classified by range:
```
< 1024       →  Well-Known Port     (MEDIUM risk)
1024–49151   →  Registered Port     (LOW risk)
49152+       →  Dynamic/Private     (LOW risk)
```

---

## `> DISCLAIMER`

```
╔══════════════════════════════════════════════════════════════════════╗
║  [!] FOR EDUCATIONAL & AUTHORIZED SECURITY TESTING PURPOSES ONLY    ║
║                                                                      ║
║  Always obtain explicit permission before scanning any network       ║
║  or host. Unauthorized port scanning may be illegal in your          ║
║  jurisdiction. The author assumes no liability for misuse.           ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

<div align="center">

`[ SYSTEM READY ]` — `[ THREADS ARMED ]` — `[ AWAITING TARGET ]`

**Python Project by V.Mouli**

</div>
