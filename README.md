<div align="center">

<img src="assets/banner.png" alt="AEGIS — Divine Network Shield" width="100%" />

<br/><br/>

[![Latest Release](https://img.shields.io/github/v/release/ShiTmoZ/Aegis-Client?color=2e9fdb&label=Release&style=for-the-badge)](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D4?style=for-the-badge&logo=windows)](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)
[![Protocols](https://img.shields.io/badge/Protocols-VLESS%20%7C%20VMess%20%7C%20Trojan%20%7C%20SS%20%7C%20Hy2-blueviolet?style=for-the-badge)](#)
[![Core](https://img.shields.io/badge/Core-sing--box%20v1.14.2-blue?style=for-the-badge)](https://github.com/SagerNet/sing-box)
[![Driver](https://img.shields.io/badge/TUN-Wintun%200.14.1-emerald?style=for-the-badge)](https://www.wintun.net)
[![AI Engine](https://img.shields.io/badge/AI-Thompson%20Bandit%20%2B%20Genetic-gold?style=for-the-badge)](#)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen?style=for-the-badge)](#)

<br/>

**AEGIS** is an autonomous, ultra-lightweight, and luxury DPI evasion client for Windows.  
Engineered from the ground up for high-durability censorship circumvention across aggressive state-level firewalls.  
**Delivered as a single, self-contained standalone executable (`flow.exe`). Zero installers. Zero .NET dependencies.**

</div>

---

## ⚡ Highlights

- **Universal Multi-Protocol Engine (v2rayN Parity)**: Natively parses and runs all standard proxy links — `vless://` (Reality, WS, gRPC), `vmess://` (Base64 JSON), `trojan://`, `ss://` (Shadowsocks SIP002 & legacy), and `hysteria2://` / `hy2://`.
- **Single Executable (`flow.exe`)**: Everything needed is embedded in one portable binary (~35 MB). No runtime installation, Python, or .NET required.
- **Embedded Production Core**: Integrates official **sing-box v1.14.2** and signed **Wintun 0.14.1** virtual network driver with modern declarative rule-based sniffing.
- **Autonomous Neural & Genetic Fragment Slicing**: Dynamically discovers optimal TLS packet boundaries to evade deep packet inspection while strictly avoiding anomalous patterns that trigger ISP heuristic scanners.
- **Carrier-Split Auto-Routing**: Automatically identifies your active ISP (MCI, Irancell, Mokhaberat, Rightel) and dynamically routes through carrier-optimized endpoints.
- **Persistent Real Delay RTT**: Native v2rayN-style persistent HTTP latency tracking directly through the active tunnel.
- **Safe-by-Default Architecture**: Fragment is OFF by default for direct high-speed connections and can be toggled on with one click as an evasive weapon. Clean IP scanning is automatically bypassed on direct server IPs.
- **Live Diagnostics Console**: Integrated real-time log viewer directly accessible from the dashboard header.
- **Zero-Footprint OpSec**: Guaranteed fail-safe Windows registry proxy cleanup upon exit. Zero leftover dead proxy configurations.

---

## 📊 Technical Comparison

| Feature / Metric | **AEGIS** (`flow.exe`) | **v2rayN** | **Clash Verge Rev** | **NekoBox** |
| :--- | :---: | :---: | :---: | :---: |
| **Distribution** | **Single Portable Binary** | Multi-file ZIP archive | Installer / Large bundle | Multi-file ZIP archive |
| **Dependencies** | **Zero** (Native Go AOT) | .NET Desktop Runtime 8.0+ | WebView2 + C++ Redist | C++ Redist + Qt |
| **RAM Footprint** | **~25 – 35 MB** | 180 – 350 MB | 250 – 500 MB | 120 – 220 MB |
| **Cold Startup Time** | **< 200 ms** | 2 – 5 seconds | 3 – 6 seconds | 1 – 3 seconds |
| **Protocol Support** | **VLESS, VMess, Trojan, SS, Hy2** | VLESS, VMess, Trojan, SS | Clash-rule profiles | VLESS, VMess, Trojan, SS |
| **ISP Auto-Selection** | **Automated Carrier Split** | Manual node selection | Heuristic rule-based | Manual / Group |
| **DPI Adaptation** | **Neural Thompson Bandit + Genetic** | Static configuration | Static configuration | Static configuration |
| **Registry Recovery** | **Guaranteed Fail-Safe Rollback** | Often leaves broken proxy | Manual reset required | Often leaves broken proxy |
| **Code Structure** | **Native Machine Code (`-s -w`)** | Managed MSIL (C# dnSpy-able) | Electron / Webview frontend | C++ Native |

---

## 🚀 Quick Start

1. **Download**: Grab the latest release of **[`flow.exe`](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)**.
2. **Launch**: Double-click `flow.exe` — no administrator prompt required for default System Proxy mode.
3. **Configure**: Paste any standard config link (`vless://`, `vmess://`, `trojan://`, `ss://`, `hy2://`, or subscription URL) into Settings (`⚙`).
4. **Connect**: Click the **Tap to Connect** central shield orb.

> **Exiting Cleanly**: Click the **✕** button on the header or right-click the taskbar tray drop icon and select **Quit AEGIS**. System proxy settings are wiped clean and restored instantly.

---

## 🧠 Autonomous Neural & Genetic Optimization Engine

AEGIS does not treat censorship circumvention as a guessing game. It features an integrated **Reinforcement Learning Multi-Armed Bandit (MAB)** optimizer paired with an **Adaptive Genetic Algorithm**:

### 1. The Art of Fragment Evasion vs. Anomaly Detection
DPI middleboxes inspect the TLS `ClientHello` packet to detect the SNI (Server Name Indication). While slicing packets can defeat naive SNI filters, crude or static fragmentation generates distinct transport-layer anomalies that ISP heuristic classifiers flag, leading to packet throttling or silent blackholing.
AEGIS solves this through dynamic evolution:
- **Genetic Exploration**: The engine mutates packet boundary cutoffs (`pktMin`, `pktMax`) and inter-packet delay intervals (`delayMs`) across micro-generations.
- **Fitness Evaluation**: Each parameter set is evaluated against real throughput, jitter, and TCP RST/timeout events:
  $$\text{Fitness} = w_1 \cdot \text{Throughput} - w_2 \cdot \text{RTT} - w_3 \cdot \text{PacketLoss} - w_4 \cdot \text{Jitter}$$
- **Thompson Sampling**: Models packet distributions as a stochastic multi-armed bandit with **Beta Priors** $\text{Beta}(\alpha, \beta)$, striking the perfect balance between testing evasive boundaries and exploiting proven stable paths.

### 2. Intelligent Direct vs. CDN Awareness
- **Direct Server IPs**: When connected directly to a VPS or dedicated proxy IP, AEGIS automatically bypasses Clean IP scanning to eliminate useless background probes and save system resources.
- **Cloudflare / CDN Workers**: Automatically activates the Clean IP latency ranking engine to discover unthrottled Anycast edge IPs.

### 3. User Sovereignty & Safety
- **Strict Default OFF**: TLS Fragment is disabled by default to provide maximum speed and minimum latency on unblocked routes.
- **Weapon on Demand**: When encountering network throttling or SNI blocks, flipping the interactive Fragment switch activates the AI evasion suite.
- **Manual Lock**: Users can freeze parameters at any time via the **Lock Manual Values** control.

---

## 🛡️ Core Architecture

### 1. Self-Contained Standalone Executable
AEGIS embeds the complete 64-bit **sing-box v1.14.2** engine and the signed **Wintun 0.14.1** driver directly inside `flow.exe`. It extracts runtime components to an isolated temporary namespace with zero disk residue upon termination.

### 2. Universal Protocol Ingestion
No manual protocol selection or conversion needed:
- **VLESS**: Supports Reality (`xtls-rprx-vision`), WebSocket, gRPC, and raw TCP.
- **VMess**: Decodes standard Base64 JSON configurations across all transports.
- **Trojan**: Full TLS support with custom SNI and ALPN negotiation.
- **Shadowsocks**: Supports both modern SIP002 URIs and legacy Base64 formats.
- **Hysteria2**: High-throughput UDP obfuscation for severe loss conditions.

### 3. Dual Routing Modes
- **System Proxy Mode (Default)**: Runs seamlessly with standard user privileges. Configures the loopback HTTP/SOCKS5 proxy (`127.0.0.1:2080`) for all Windows browsers, Telegram, and standard desktop applications.
- **Virtual TUN Mode**: When executed with elevated permissions (*Run as Administrator*), AEGIS initializes the high-speed Wintun virtual network adapter, routing all system UDP and TCP traffic with near-zero overhead.

### 4. Path MTU Blackhole Protection & DNS Caching
- **1350 MTU Clamping**: Specifically tuned for Iranian telecom backbones to eliminate silent TCP packet drops caused by encapsulation overhead.
- **Zero-Latency In-Memory DNS**: Built-in 4,096-record DoH cache eliminates round-trip lookup delays for complex, asset-heavy modern web apps.

---

## 📜 Rollback-Safe 10-Release Changelog

| Version | Release Date | Key Architecture Changes & Milestones |
| :--- | :---: | :--- |
| **v2.1.0** | **2026-10-04** | **Universal Multi-Protocol Engine**: Added full support for `vless://`, `vmess://`, `trojan://`, `ss://`, and `hy2://` with v2rayN parity. Upgraded embedded core to **sing-box v1.14.2** with modern declarative rule-based sniffing. Unlocked glassmorphic TLS Fragment UI with autonomous Genetic & Thompson Bandit tuning. Direct IP clean-scan bypass. |
| **v2.0.2** | 2026-10-01 | **Production Deployment**: Standalone `flow.exe` packaging (~35MB), 2x2 HUD telemetry grid (RTT, Packet Loss, Speed), Live Diagnostic Console modal, and trailing-whitespace input auto-sanitizer. |
| **v2.0.1** | 2026-09-30 | Integrated live system diagnostics log viewer modal and improved UI IPC responsiveness. |
| **v2.0.0** | 2026-09-30 | **Architecture Revolution**: Migrated from python CLI to standalone Go AOT binary with embedded Wintun L3 engine. Rebranded to AEGIS Divine Network Shield. |
| **v1.2.0** | 2026-09-28 | Introduced AI Lab web dashboard (`127.0.0.1:41718`), background evolutionary loop, and graceful proxy cleanup signal interception. |
| **v1.1.2** | 2026-09-26 | Persistent real delay RTT tracking through the active tunnel and fail-safe system proxy recovery. |
| **v1.1.0** | 2026-09-23 | Carrier-split intelligent routing engine for MCI, Irancell, and Mokhaberat telecom networks. |
| **v1.0.4** | 2026-09-20 | MTU clamping to 1350 bytes to mitigate silent packet drop blackholes in Middle Eastern ISP gateways. |
| **v1.0.2** | 2026-09-15 | Embedded DoH cache with 4,096 records and randomized uTLS Chrome fingerprint emulation. |
| **v1.0.0** | 2026-09-10 | Initial core client release with raw socket probes and SQLite disruption memory model. |

---

## 🔒 Security & Privacy Guarantees

- **No Remote Telemetry**: AEGIS sends zero usage statistics, analytics, or behavioral telemetry to any third party.
- **In-Memory Sanitization**: Subscription tokens and intermediate configuration objects are actively zeroed out in RAM using `SecureBuffer`.
- **Fail-Safe Registry Protection**: A multi-layered signal interceptor (`os.Interrupt`, `syscall.SIGTERM`, UI close events) ensures `ClearWindowsSystemProxy` is executed even during abrupt system logoffs.

---

<div align="center">

<sub>AEGIS · Divine Network Shield · High-Durability Censorship Circumvention</sub>

</div>
