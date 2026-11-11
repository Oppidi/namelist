# Tracker & Telemetry Blocklist

适用于 AdGuard Home、Pi-hole 等 DNS 过滤器的规则仓库。专注于拦截特定场景的追踪遥测、设备管理与后台自注册行为。

<p align="center">
  <a href="README.md">English</a> •
  <b>中文</b>
</p>

---

## 📋 规则类型概览

本项目目前按功能模块细分规则分类。各规则集的具体收录范围、目标场景与技术说明请查阅对应子目录文档：

| 类型 / 模块 | 目录位置 | 覆盖范围与说明 | 状态 |
| :--- | :--- | :--- | :--- |
| **运营商设备管理与自注册 (Carrier DM)** | [`Device_Management/`](Device_Management/README-zh-hans.md) | 仅收录特定国家/地区（中国大陆、伊朗等）运营商终端自注册 (ZZHC)、移动设备管理 (DM) 平台及基带硬件指纹遥测（不影响正常上网、通话与短信） | 🟢 维护中 |

---

## 🔗 纯文本订阅链接

直接复制下方纯文本链接，添加到 AdGuard Home 的 **过滤器** -> **DNS 黑名单** 中即可：

### 1. 运营商设备管理与自注册 (Carrier DM)
- **AdGuard Home / DNS Filter 格式**:
```text
https://raw.githubusercontent.com/Oppidi/namelist/main/Device_Management/cn-dm-adguard.txt
```

---

## 📂 子层分点导航

各分类的技术背景、协议机制与规则说明请参阅各自分层文档：

* **[Device_Management (运营商设备管理与自注册)](Device_Management/README-zh-hans.md)**
  * 收录范围声明（中国大陆、伊朗等特定国家/地区）
  * 简介与 Carrier Explode 机制参考
  * 覆盖范围与 AdGuard Home 配置方式

---

## 🤖 自动化更新与维护

本项目通过 GitHub Actions / GitHub Agents 定期检测、去重与验证域名有效性，保持列表持续更新。
