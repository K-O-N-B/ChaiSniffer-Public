# 柴嗅 / ChaiSniffer

**柴嗅** 是一款浏览器扩展 + Windows 本机组件，用于在网页上发现媒体地址，并在本机下载或交给外部播放器打开。

> 扩展可从 **Microsoft Edge 加载项** 安装；**本机 Host 需单独下载**（见下方 Releases）。  
> 本产品 **不提供扩展与 Host 源代码**；本仓库仅公开用户文档与安装包。

---

## 你能做什么

| 能力 | 说明 |
|------|------|
| 嗅探 | 在当前页面发现 HLS / DASH / 直链等媒体地址 |
| 本机下载 | 非 DRM 的 HLS（含 AES-128）分轨或合并下载（需 Host + ffmpeg） |
| 外部播放 | 将 URL、Cookie、Referer 等交给 mpv / VLC / PotPlayer |
| 安全边界 | **拒绝** Widevine 等商业 DRM 内容 |

---

## 快速开始（Windows，完整功能）

1. 安装 **柴嗅** 扩展（Edge 商店或开发者加载）。
2. 打开扩展 **设置**，复制 **扩展 ID**。
3. 从 **[Releases · 最新版](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest)** 下载 **Windows 本机组件** zip 并解压。
4. 运行 `native-host\setup-bridge.cmd`，粘贴扩展 ID。
5. 在设置页点击 **运行完整自检**，确认 Host / ffmpeg / 播放器 均为 ✓。
6. 打开目标页面，点击工具栏柴嗅图标，在资源列表中下载或播放。

详细步骤 → [docs/INSTALL_HOST.md](docs/INSTALL_HOST.md)

---

## 平台支持

| 平台 | 扩展（嗅探/列表） | 本机 Host（下载/播放） |
|------|-------------------|------------------------|
| **Windows 10/11** | ✅ | ✅（主要测试环境） |
| **macOS** | 可能可用 | ⏸ **暂未完整支持** |
| **Linux** | 可能可用 | 未验收 |

详见 [docs/TEST_ENV.md](docs/TEST_ENV.md)

---

## 重要提醒

- **扩展 ≠ Host**：商店只能安装浏览器部分；下载、合并、调用播放器需要本机程序。
- **商店版扩展 ID 与开发版不同**：安装 Host 时必须使用 **设置页显示的 ID**。
- **版权与合规**：请仅下载您有权保存或离线观看的内容；本工具不绕过 DRM，也不鼓励侵权。
- **隐私**：处理均在本地，详见 [PRIVACY.md](PRIVACY.md)。

---

## 链接

| 内容 | 地址 |
|------|------|
| 本机组件下载 | [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) |
| 安装说明 | [INSTALL_HOST.md](docs/INSTALL_HOST.md) |
| 测试环境 | [TEST_ENV.md](docs/TEST_ENV.md) |
| 隐私政策 | [PRIVACY.md](PRIVACY.md) |

---

## 反馈

在 [Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues) 提交问题时请附上：系统版本、Edge 版本、扩展版本、是否已安装 Host、自检结果截图。
