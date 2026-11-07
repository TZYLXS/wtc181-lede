# TP-Link WTC181 LEDE 固件

OpenWrt/Lede 固件 for TP-Link WTC181（电信版 AX1800，MT7621AT + MT7905DAN + MT7975BN）。

## 固件信息

| 项目 | 内容 |
|---|---|
| 源码 | [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)（Lean） |
| Commit | `e2c1ff04` |
| 版本 | 24.10.5 |
| 目标 | ramips / mt7621（mipsel 24kc musl） |
| 内核 | Linux 5.10.271 |
| 闪存布局 | 32MB SPI NOR（换flash后），squashfs + overlay |
| 无线 | MT7915E 驱动 + kmod-mt7915e，支持 WiFi6 / WPA3 |

## 设备

- **TP-Link WTC181**（电信版 AX1800）
- 同板：EF1210 / 水星 X18G / XDR1860
- CPU: MT7621AT, 128MB DDR3
- 需更换为 32MB SPI NOR 闪存（原板 128MB NAND）

## 刷机

详见 [WTC181-刷机说明.md](WTC181-刷机说明.md)。

固件文件在 [Releases](../../releases) 页面下载。

## 文件说明

| 文件 | 用途 |
|---|---|
| `openwrt-ramips-mt7621-tplink_wtc181-squashfs-sysupgrade.bin` | 主刷机固件（Breed 刷入） |
| `openwrt-ramips-mt7621-tplink_wtc181-initramfs-kernel.bin` | TTL 内存启动调试镜像（救砖用） |
| `*.manifest` | 已安装软件包清单 |
| `*sha256sums.txt` | SHA256 校验值 |
