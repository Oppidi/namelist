# Tracker & Telemetry Blocklist

DNS blocklists tailored for AdGuard Home, Pi-hole, and DNS filters. Focused on blocking targeted telemetry, carrier device management, and background self-registration.

<p align="center">
  <b>English</b> •
  <a href="README-zh-hans.md">中文</a>
</p>

---

## 📋 Blocklist Categories

This repository organizes filter rules into modular categories. For specific scope, target environments, and technical documentation of each category, see the respective subdirectories:

| Category / Module | Directory | Scope & Description | Status |
| :--- | :--- | :--- | :--- |
| **Carrier Device Management (DM)** | [`Device_Management/`](Device_Management/README.md) | Strictly covers carrier terminal self-registration (ZZHC), Device Management (DM) platforms, and baseband hardware telemetry in specific countries/regions (Mainland China, Iran, etc.); does not affect regular cellular data, voice calls, or SMS | 🟢 Active |

---

## 🔗 Plain Text Subscription Links

Copy and paste the plain text URLs below directly into AdGuard Home under **Filters** -> **DNS blocklists**:

### 1. Carrier Device Management (DM)
- **AdGuard Home / DNS Filter format**:
```text
https://raw.githubusercontent.com/Oppidi/namelist/main/Device_Management/cn-dm-adguard.txt
```

---

## 📂 Subdirectory Navigation

Detailed background research, protocol mechanisms, and sub-rule specifications are documented within each subfolder:

* **[Device_Management/](Device_Management/README.md)**
  * Scope Notice (Mainland China, Iran, and specific regional networks)
  * Overview & Carrier Explode references
  * Coverage scope & AdGuard Home configuration steps

---

## 🤖 Automated Maintenance

Filter rules are maintained and validated using GitHub Actions / GitHub Agents for syntax checking, deduplication, and domain availability verification.
