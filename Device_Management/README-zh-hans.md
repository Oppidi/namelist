# 运营商设备管理与自注册拦截规则 (Carrier DM Telemetry Blocklist)

<p align="center">
  <a href="README.md">English</a> •
  <b>中文</b>
</p>

用于阻断特定国家/地区（中国大陆、伊朗等）运营商移动设备管理 (DM) 平台及终端静默自注册遥测的 AdGuard Home 规则。

> [!IMPORTANT]
> **收录范围声明**：本项目目前仅收录存在强制性设备画像或入网核验特征的特定国家/地区（中国大陆、伊朗等）运营商 DM 平台与终端自注册域名。

---

## 简介

在特定国家/地区网络环境下，终端在开机或插卡时，基带及系统底层会静默向运营商 DM 平台上传硬件指纹（IMEI、IMSI、基站小区信息等）用于设备画像与追踪。底层机制参考 [Carrier Explode - China Self-Registration](https://carrierexplode.com/wiki/ios/china-self-registration)。

本项目旨在屏蔽此类遥测行为。拦截后**不影响常规数据上网、电话及短信服务**。

---

## 覆盖范围

- **中国大陆 (Mainland China)**：中国移动、中国电信、中国联通的终端自注册 (ZZHC) 与设备管理平台（包含高通基带 `ds_autoreg` 上报端点、CoAP 遥测服务及产品库平台）
- **伊朗 (Iran)**：MCI、MTN Irancell 等本土运营商后台遥测与设备核验节点
- 其他具备强制入网自注册特征的运营商 DM 域名

---

## 纯文本订阅地址

```text
https://raw.githubusercontent.com/Oppidi/namelist/main/Device_Management/cn-dm-adguard.txt
```

---

## AdGuard Home 配置方式

1. 进入 AdGuard Home 控制台 -> **过滤器 (Filters)** -> **DNS 黑名单 (DNS blocklists)**。
2. 点击 **添加黑名单 (Add blocklist)** -> **添加自定义列表 (Add a custom list)**。
3. 填入上述纯文本规则订阅地址保存即可。本地或私有部署可直接引用本目录下的 `cn-dm-adguard.txt`。
