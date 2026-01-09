# 🔍 Detecting Wi-Fi Deauthentication Attacks Using Kismet

This repository demonstrates how **Kismet**, an open-source wireless intrusion detection system (IDS), can be used to **detect, analyze, and mitigate Wi-Fi deauthentication attacks** in a controlled and ethical environment.

The project focuses on **attack detection and analysis**, not exploitation. All demonstrations are performed using **PCAP replay** or **authorized lab networks**.

---

## 🧠What is Kismet?

Kismet is a passive wireless network detector, sniffer, and intrusion detection system that supports:

- Wi-Fi (IEEE 802.11)
- Bluetooth
- Zigbee and other RF protocols

Kismet captures and analyzes wireless traffic without transmitting packets, making it ideal for stealthy monitoring and attack detection.

---

## Uses of Kismet 🎯

- Wireless network discovery
- Detection of deauthentication and disassociation attacks
- Rogue access point detection
- Wireless security auditing
- Network monitoring and forensics
- Academic and research demonstrations

---

## What is a Wi-Fi Deauthentication Attack ⚠️?

A deauthentication attack exploits unprotected 802.11 management frames to forcibly disconnect clients from a Wi-Fi access point by sending spoofed deauthentication packets.

Such attacks are commonly used in:
- Denial-of-Service (DoS)
- Evil Twin attacks
- WPA/WPA2 handshake capture attempts

---

## Demo Environment Overview

This repository demonstrates two approaches for observing deauthentication attacks using Kismet.

### 1. PCAP Replay (Recommended)

This method replays a pre-captured PCAP file containing deauthentication frames.  
No special hardware is required.

Steps:
1. Place the PCAP file in your Linux or WSL environment
2. Run Kismet in replay mode:
   ```bash
   kismet -c /path/to/deauth_attack.pcap
3. Open the Kismet Dashboard

After launching Kismet, open the web interface using the following URL: http://localhost:2501/
Observe alerts such as **Deauthentication Flood** and **NOCLIENTMFP** in the Alerts/Events tab.

---

### 2. Live Lab Attack (Authorized Networks Only)

This method is performed **only in isolated or permitted lab environments**.

## Tools Used
- **Kismet** (Detection)
- **wifi-deauth / aireplay-ng** (Attack simulation)

Live attack steps and screenshots are documented in: pdf above in this repository.

---

## Interpreting Kismet Alerts

Common alerts observed during deauthentication attacks include:

### Deauthentication Flood
Indicates multiple spoofed deauthentication frames detected within a short time period.

### NOCLIENTMFP
Indicates that Management Frame Protection (MFP) is not enabled, making the client or access point vulnerable to spoofed deauthentication and disassociation attacks.

Each alert provides:
- Affected access point (AP) and client MAC addresses
- Event timestamps
- Severity level
- Recommended actions

---

## Output and Evidence

This repository includes:

- Kismet dashboard screenshots
- Detected devices and affected clients
- Alert logs and event summaries
- PCAP replay results

All outputs are stored in the following directory: kismet file in this repository


---

## Mitigation Techniques

Recommended defenses against deauthentication attacks include:

- Enable **802.11w (Management Frame Protection)**
- Use **WPA3** security
- Disable **WPS**
- Use strong Wi-Fi passphrases
- Keep router firmware updated
- Monitor wireless networks using IDS tools like **Kismet**

Detailed mitigation notes are available in the attached PDF and theory documentation.

---
## Reference Links

- **Kismet on Kali Linux (Tool Detection & Usage)**  
  https://www.kali.org/tools/kismet/

- **About Kismet (Wikipedia)**  
  https://en.wikipedia.org/wiki/Kismet_(software)

- **Kismet Development & Plugin Documentation**  
  https://www.kismetwireless.net/docs/dev/plugins/
---

## Disclaimer

This project is intended strictly for **educational and defensive purposes**.  
Do not perform wireless attacks on networks without explicit authorization.

---

## Connect With Me

- 📌 **YouTube**: [Sarah Rachel Coder](https://www.youtube.com/@sarahrachelcoder)
- 📌 **Instagram**: [engineering_codex](https://www.instagram.com/engineering_codex?igsh=ZjI2YTh1YjlhcTRu)
- 📌 **GitHub**: [sarah131](https://github.com/sarah131)
- 📌 **Medium**: [@sarahrachel831](https://medium.com/@sarahrachel831)
- 📌 **LinkedIn**: [Sarah Rachel](https://www.linkedin.com/in/sarah-rachel-65532720b)

---

⭐ If this repository helped you, don’t forget to **star** it and share with your peers!


