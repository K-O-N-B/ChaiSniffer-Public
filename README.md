# 柴嗅 / ChaiSniffer

**Languages:** [简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

**柴嗅** 是一款浏览器扩展 + Windows 辅助应用：在网页上发现媒体地址，在本机下载或交给播放器打开。

> 扩展可从 **Microsoft Edge 加载项** 安装；**辅助应用需单独下载**（见 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest)）。

---

## 快速开始（Windows）

1. 安装 **柴嗅** 扩展。
2. 打开 **设置** → 复制 **扩展 ID**。
3. 下载并解压 **辅助应用**（可解压到任意文件夹）。
4. 运行 `native-host\setup-bridge.cmd`，粘贴扩展 ID。
5. 设置页 **检查是否安装成功** → 全部 ✓。
6. 在 **播放器设置** 中配置 mpv 或 [NeoPlayer](https://github.com/K-O-N-B/NeoPlayer/releases/latest)。

详细说明 → [docs/zh-CN/INSTALL_HOST.md](docs/zh-CN/INSTALL_HOST.md)

---

## 文档

| 语言 | 安装 | 测试环境 | 隐私 |
|------|------|----------|------|
| 简体 | [INSTALL_HOST](docs/zh-CN/INSTALL_HOST.md) | [TEST_ENV](docs/zh-CN/TEST_ENV.md) | [PRIVACY](PRIVACY.md) |
| 繁體 | [INSTALL_HOST](docs/zh-TW/INSTALL_HOST.md) | [TEST_ENV](docs/zh-TW/TEST_ENV.md) | [PRIVACY.zh-TW](PRIVACY.zh-TW.md) |
| English | [INSTALL_HOST](docs/en/INSTALL_HOST.md) | [TEST_ENV](docs/en/TEST_ENV.md) | [PRIVACY.en](PRIVACY.en.md) |

---

## 能力概览

| 能力 | 说明 |
|------|------|
| 嗅探 | 发现 HLS / DASH / 直链 |
| 本机下载 | 非 DRM HLS（需辅助应用） |
| 外部播放 | mpv / VLC / PotPlayer / NeoPlayer |
| 安全 | 拒绝商业 DRM |

---

## 反馈

[GitHub Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues)
