# 本机组件安装说明（Host）

> **柴嗅 / ChaiSniffer** 分两部分：**浏览器扩展**（嗅探列表）+ **本机 Host**（下载、合并、调用播放器）。  
> 从 Edge 商店安装的用户也需要单独安装 Host，扩展本身不会自动带上 Host。

---

## 下载地址

| 内容 | 链接 |
|------|------|
| **Windows 安装包（推荐）** | [GitHub Releases · 最新版](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) |
| 本文档 | [INSTALL_HOST.md](https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/docs/INSTALL_HOST.md) |
| 测试环境说明 | [TEST_ENV.md](./TEST_ENV.md) |

Release 包预期包含（以实际上传为准）：

- `native-host/` 目录
- `setup-bridge.cmd`（Windows 一键登记 Native Messaging）
- 内置 `bin/ffmpeg.exe`（一般无需单独安装 ffmpeg）
- 简短 `README.txt`

---

## Windows 安装步骤

1. 从 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) 下载 **Windows 本机组件** zip 并解压。
2. 打开柴嗅扩展 **设置**，复制 **扩展 ID**。
3. 双击 `native-host\setup-bridge.cmd`，粘贴扩展 ID。
4. 在设置里点 **运行完整自检**，确认 Host / ffmpeg / 播放器 均为 ✓。
5. 若从 **Edge 商店** 安装扩展，扩展 ID 与开发版不同 — 安装 Host 时必须粘贴**商店版**设置页里的 ID。

---

## ffmpeg 与播放器

| 组件 | 说明 |
|------|------|
| **ffmpeg** | 用于 HLS 解密合并、分轨混流。Release 包若已带 `bin\ffmpeg.exe` 一般无需再装。 |
| **播放器** | 在扩展设置里填写 mpv / VLC / PotPlayer 等路径。Windows 推荐 mpv。 |

---

## macOS 支持程度（当前）

| 能力 | macOS |
|------|--------|
| 扩展：嗅探、资源列表、Popup | 可能可用 |
| 本机 Host：下载 / 合并 / 外调播放器 | ⏸ **暂未完整支持** |

Mac 用户可先使用扩展嗅探与复制链接；完整本机下载请用 **Windows**。

---

## 常见问题

**Q：为什么商店扩展还要再装 Host？**  
A：商店只能装浏览器扩展；在你电脑上跑 ffmpeg、写文件、开 mpv 需要本机程序，微软允许这种组合，但需用户自行安装。

**Q：代码是否开源？**  
A：本公开仓库提供文档与安装包；扩展与 Host **源代码不对外公开**。

**Q：下载失败 / 桥接未连接？**  
A：确认已运行 `setup-bridge.cmd`、扩展 ID 一致、Edge 已重新加载扩展，并在设置页运行自检。
