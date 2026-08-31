# 柴嗅 / ChaiSniffer

**Languages:** [简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

**柴嗅** 是一款浏览器扩展 + Windows 辅助应用：在网页上发现媒体地址，在本机下载或交给**外部播放器**打开。

> 扩展可从 **Microsoft Edge 加载项** 安装（**v0.9.16 审核准备中**）；**辅助应用需单独下载**（见 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest)）。

**当前版本：** 扩展 **0.9.16** · 辅助应用 **host-v0.9.14.1+** · [更新说明](RELEASE_NOTES/v0.9.16.md)

---

## 为什么做柴嗅

浏览器里的播放器往往受网页限制，画质、流畅度、字幕和 AI 翻译等能力有限。**柴嗅 负责嗅探视频地址并桥接到本机**；具体播放体验交给您安装的播放器（如 mpv），由播放器提供：

- 更好的 **画质与流畅度**（超分、插帧、着色器等，取决于播放器配置）
- 播放器侧的 **AI 翻译、字幕** 等增强能力
- 对 **重要、有意义的内容** 进行本机保存（请仅保存您有权保存的视频）

柴嗅 **不内置** 播放器功能，也不绕过 DRM；它只做「发现地址 → 本机下载或交给播放器」。

---

## 播放器说明

| 播放器 | 建议 |
|--------|------|
| **[mpv](https://mpv.io/)** | **当前推荐。** 主要测试环境，HLS / Cookie / 分轨桥接兼容性最好。 |
| **[NeoPlayer](https://github.com/K-O-N-B/NeoPlayer)** | 作者自用播放器，**仍在开发中**，之后会在此仓库上传 Release。现阶段请先使用 mpv。 |
| PotPlayer / VLC 等 | 可在设置中添加，但 **兼容性未全面验证**，部分站点可能无法播放或下载。 |

画质增强、AI 翻译、字幕样式等均由 **播放器及其插件/脚本** 负责，不在柴嗅扩展内实现。

---

## 快速开始（Windows）

1. 安装 **柴嗅** 扩展。
2. 打开 **设置** → 复制 **扩展 ID**。
3. 下载并解压 **辅助应用**（可解压到任意文件夹）。
4. 运行 `native-host\setup-bridge.cmd`，粘贴扩展 ID。
5. 设置页 **检查是否安装成功** → 全部 ✓。
6. 在 **播放器设置** 中配置 **[mpv](https://mpv.io/)**（推荐）。NeoPlayer 开发完成后会另行发布。

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
| 浮动图标 | 视频上一键打开播放器（v0.9.16，可在设置关闭） |
| 本机下载 | 非 DRM HLS（需辅助应用） |
| 外部播放 | **推荐 mpv**；NeoPlayer 开发中；其他播放器兼容性不确定 |
| 安全 | 拒绝商业 DRM |

---

## 反馈

[GitHub Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues)
