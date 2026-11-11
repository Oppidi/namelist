# Carrier DM Telemetry Blocklist

<p align="center">
  <b>English</b> •
  <a href="README-zh-hans.md">中文</a>
</p>

AdGuard Home rules designed to block carrier Device Management (DM) platforms and silent terminal self-registration telemetry in specific countries/regions (Mainland China, Iran, etc.).

> [!IMPORTANT]
> **Scope Notice**: This module strictly covers carrier DM platforms and self-registration domains in specific countries/regions (such as Mainland China, Iran, etc.) that enforce mandatory device profiling or enrollment telemetry.

---

## Overview

In certain regional network environments, baseband firmware and system components silently transmit hardware fingerprints (IMEI, IMSI, base station cell IDs, etc.) to carrier DM servers upon device boot or SIM insertion for device profiling and tracking. Underlying mechanisms reference [Carrier Explode - China Self-Registration](https://carrierexplode.com/wiki/ios/china-self-registration).

This list blocks these telemetry requests. Blocking them **does not affect normal cellular data, phone calls, or SMS services**.

---

## Coverage Scope

- **Mainland China**: Terminal self-registration (ZZHC) and device management platforms for China Mobile, China Telecom, and China Unicom (including Qualcomm baseband `ds_autoreg` endpoints, CoAP telemetry, and device databases)
- **Iran**: Backend telemetry and verification nodes for local carriers such as MCI and MTN Irancell
- Other carrier DM domains exhibiting mandatory network enrollment self-registration

---

## Plain Text Subscription Link

```text
https://raw.githubusercontent.com/Oppidi/namelist/main/Device_Management/cn-dm-adguard.txt
```

---

## AdGuard Home Setup

1. Open the AdGuard Home dashboard -> **Filters** -> **DNS blocklists**.
2. Click **Add blocklist** -> **Add a custom list**.
3. Paste the plain text subscription link above and save. For local deployments, directly reference `cn-dm-adguard.txt`.
