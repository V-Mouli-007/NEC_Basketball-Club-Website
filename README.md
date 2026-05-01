<div align="center">
 
# 🔍 YourPortScanner
 
### `[ REAL-TIME NETWORK PORT INTELLIGENCE TOOL ]`

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.1.3-black?style=for-the-badge&logo=flask&logoColor=white)
![Security](https://img.shields.io/badge/Security-Tool-red?style=for-the-badge&logo=hackthebox&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

<div align="center">

**Python Project by V.Mouli**

</div>

## 📖 About the Project

**YourPortScanner** is a web-based port scanning tool that lets you scan any target host for open TCP ports in real time. It features an elegant cyberpunk-inspired UI with neon glows, scanline overlays, and live streaming results — making security reconnaissance both powerful and visually engaging.

Results include not just open/closed status, but also the **service name**, **risk level**, and a **detailed risk description** for each scanned port — powered by a built-in port intelligence database.

---

## ✨ Features

<div align="left">

- 🌐 **Real-Time Scanning** — Results stream live to the browser using Server-Sent Events (SSE)
- ⚡ **Multi-threaded Engine** — Scans up to 200 threads concurrently for blazing-fast results
- 🎯 **Flexible Port Selection** — Scan specific ports or the full range (1–65535)
- 🛡️ **Risk Intelligence** — Every port result includes service name, risk level (`LOW` / `MEDIUM` / `HIGH` / `CRITICAL`), and a description of potential vulnerabilities
- 🖥️ **Cyberpunk Web UI** — Neon-lit, grid-background interface with animated scanlines
- 🔢 **Port Range Support** — Comma-separated custom ports or all-ports full scan mode
- 🌍 **Hostname Resolution** — Accepts both IP addresses and domain names

---

## 🗂️ Project Structure

<div align="left">

```
YourPortScanner/
├── app.py                  # 🐍 Main Flask application & scanning logic
├── templates/
│   └── index.html          # 🎨 Cyberpunk-themed frontend UI
└── venv/                   # 📦 Python virtual environment
```

---

## 🛠️ Tech Stack

<div align="left">

| Technology | Purpose |
|---|---|
| 🐍 **Python 3** | Core language |
| 🌶️ **Flask 3.1.3** | Web framework & SSE streaming |
| 🔌 **socket** | TCP port connection testing |
| 🧵 **threading** | Concurrent multi-threaded scanning |
| 🎨 **Tailwind CSS** | Frontend utility styling |
| 🔤 **Google Fonts** | Cyberpunk typography (Exo 2, Share Tech Mono, Rajdhani) |

---

## 📦 Dependencies

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

## 🚀 Getting Started

### 1️⃣ Clone or Extract the Project

```bash
# Extract the zip or clone your repo
cd YourPortScanner
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
```

### 3️⃣ Activate the Virtual Environment

```bash
# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 4️⃣ Install Dependencies

```bash
pip install flask
```

### 5️⃣ Run the Application

```bash
python app.py
```

### 6️⃣ Open in Browser

```
http://127.0.0.1:5000
```

---

## 🎮 How to Use

<div align="left">

1. **Enter a Target** — Type an IP address (e.g., `192.168.1.1`) or a hostname (e.g., `example.com`)
2. **Choose Scan Mode:**
   - 🎯 **Specific Ports** — Enter comma-separated port numbers (e.g., `80,443,22,3389`)
   - 🌍 **All Ports** — Scan all 65,535 TCP ports
3. **Hit Scan** — Results stream in real time to the results panel
4. **Interpret Results** — Each open port shows its service name and color-coded risk level

---

## 🛡️ Risk Level Reference

<div align="left">

| Risk Level | Color | Description |
|---|---|---|
| 🟢 **LOW** | Green | Generally safe with proper configuration |
| 🟡 **MEDIUM** | Yellow | Requires attention — potential misuse possible |
| 🟠 **HIGH** | Orange | Significant attack surface — review immediately |
| 🔴 **CRITICAL** | Red | Severe risk — should not be publicly exposed |

---

## 🔒 Port Intelligence Database

<div align="left">

The scanner includes a built-in database of **50+ well-known ports** with risk metadata, including:

- `21` FTP, `22` SSH, `23` Telnet, `25` SMTP
- `80` HTTP, `443` HTTPS, `445` SMB (EternalBlue)
- `3306` MySQL, `3389` RDP (BlueKeep), `6379` Redis
- `27017` MongoDB, `9200` Elasticsearch, `4444` Metasploit
- And many more...

Unknown ports are categorized by range:
- **< 1024** → Well-Known Port (MEDIUM)
- **1024–49151** → Registered Port (LOW)
- **49152+** → Dynamic/Private Port (LOW)

---

## ⚠️ Disclaimer

> This tool is intended for **educational purposes** and **authorized security testing only**.
> Always ensure you have explicit permission before scanning any network or host.
> Unauthorized port scanning may be **illegal** in your jurisdiction.

---

## 📄 License

This project is open for personal and educational use.

---

*🔐 Built with passion for network security and clean UI by **V.Mouli***
