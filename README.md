<div align="center">

<img src="assets/banner.png" alt="AEGIS Client Banner" width="100%">

# 🛡️ AEGIS Client
### *Next-Generation Autonomous Anti-Censorship Client for Windows*

[![Release](https://img.shields.io/github/v/release/ShiTmoZ/Aegis-Client?color=00e5ff&label=Latest%20Release&style=for-the-badge)](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20x64-blue?style=for-the-badge&logo=windows)](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)
[![Engine](https://img.shields.io/badge/Engine-Sing--box%20%2B%20Wintun-00e5ff?style=for-the-badge)](https://github.com/ShiTmoZ/Aegis-Client)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)](LICENSE)

---

**AEGIS** is a purpose-built, high-performance anti-censorship desktop client crafted for extreme network environments. Powered by an embedded **Sing-box** core and official kernel-level **Wintun** driver, AEGIS provides transparent, ultra-resilient connectivity without complex configuration.

[📥 **Download Latest Release (.exe)**](https://github.com/ShiTmoZ/Aegis-Client/releases/latest)

</div>

---

## ✨ Key Architectural Highlights

* 🛡️ **Native Layer-3 Virtual TUN (Wintun)**  
  Full operating system tunneling at the IP packet level. Seamlessly tunnels games, terminals, desktop applications, and background services without configuring manual system proxies.

* ⚡ **Intelligent Carrier-Split Routing**  
  Autonomous node selection with fine-tuned edge paths for **MCI**, **Irancell**, and fixed broadband ISPs, delivering optimal ping and zero connection drops.

* 🧬 **Adaptive TLS Record Fragmentation**  
  Advanced RFC-compliant TLS handshake obfuscation that slices `ClientHello` packets across record boundaries, evading Deep Packet Inspection (DPI) while preserving full compatibility with Anycast CDN edges.

* 🔒 **Zero-Leak Encrypted DNS**  
  Complete DNS Hijacking forwarding all local port 53 UDP/TCP queries directly to Cloudflare DoH upstream inside the encrypted tunnel, completely eliminating ISP DNS poisoning and leakage.

* 💎 **Ultra-Lightweight & Zero-Footprint**  
  Compiled into a single standalone Windows executable (~25MB runtime RAM) with no external runtimes required (no .NET, Python, or Node.js dependencies). Clean shutdown guarantees 100% restoration of Windows proxy and routing state.

---

## 🚀 Quick Start Guide

1. Download the latest `flow.exe` from the [Releases](https://github.com/ShiTmoZ/Aegis-Client/releases/latest) section.
2. Run `flow.exe` (no installation required; runs portably).
3. Paste your **AEGIS Service Key** into the settings dialog (saved securely in local app storage).
4. Select your preferred mode:
   * **Virtual TUN** *(Recommended for gaming, terminal, and all apps)*
   * **System Proxy** *(Standard browser routing)*
5. Click **Connect** and enjoy uncensored, high-speed internet.

---

## 📊 Live Network HUD

AEGIS features an integrated two-row real-time HUD providing transparent telemetry:
* **Real Delay (RTT):** Active Layer-4 TCP handshakes directly to edge servers.
* **TLS Fragment Status:** Live status of packet fragmentation engines.
* **Throughput Monitor:** Real-time download and upload transfer rates via Clash API.
* **Active Node:** Displaying carrier routing target and Anycast endpoint.

---

## 🔒 Security & Privacy Notice

* **Zero Personal Telemetry:** AEGIS does not log, inspect, or transmit user browsing history, visited domains, or credentials.
* **Safe Clean Exit:** Upon closing the application, AEGIS instantly restores Windows system proxy settings and gracefully dismantles the Wintun virtual adapter.

---

<div align="center">
<sub>Crafted with precision by <b>ShiTmoZ</b> · Designed for unrestricted access.</sub>
</div>
