# The Gate Keeper v5.0 — Enterprise Access Security Suite

![Version](https://img.shields.io/badge/version-5.0-orange.svg)
![License](https://img.shields.io/badge/license-Enterprise-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Android-lightgrey.svg)

The Gate Keeper v5.0 is an elite, multi-module cybersecurity ecosystem engineered to provide 360-degree protection, auditing, and threat response across corporate networks, mobile personnel, and endpoint workstations.

---

## 📂 Architecture & Core Modules

The platform is structured into three highly independent, production-ready modules built to cover every modern enterprise attack surface:

### 1. Central Enterprise Server & Sentinel Desktop (`.exe`)
* **Purpose:** The master monitoring hub for system administrators.
* **Key Features:** Live tracking of network clients, real-time traffic analysis, and an automated API integration with the **Safeonweb** global threat-level registry.

### 2. Hunter Mobile Security App (`.apk`)
* **Purpose:** A dedicated mobile endpoint utility for Android devices.
* **Key Features:** Secures remote and field personnel by feeding active mobile telemetry and security status logs directly back to the central server via a secure network socket.

### 3. Live Standalone Audit & Emergency Rescue Utility (`.exe`)
* **Purpose:** A plug-and-play incident response and local auditing tool.
* **Key Features:** 
  * **Option 1 (Live Audit):** Scans active network interfaces and verifies local security policies, exporting an encrypted `.txt` report.
  * **Option 2 (Emergency Rescue):** Automatically forces a hard reset of the Windows Defender Firewall back to safe corporate defaults and flushes the local DNS cache to isolate ongoing network compromises.

---

## 🛡️ Integrity & Antivirus Notice (False Positives)

Because the **Standalone Audit & Rescue Tool** requires high-level administrative privileges (`--uac-admin`) to interact directly with core network interfaces and modify Windows Firewall rules during an emergency rescue, some aggressive antivirus heuristics (such as Windows Defender) may flag the compiled executable as a false positive. 

### To ensure absolute safety and trust:
1. **Source Code Transparency:** The complete Python source code (`.py`) is provided transparently for public auditing.
2. **Verify the Hash:** Always check the cryptographic integrity of your executable. You can generate and verify the SHA-256 hash locally before running the tool:
   ```cmd
   certutil -hashfile standalone_audit_tool.exe SHA256
