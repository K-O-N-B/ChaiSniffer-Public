# 辅助应用安装说明

> **语言：** [简体中文](INSTALL_HOST.md) | [繁體中文](../zh-TW/INSTALL_HOST.md) | [English](../en/INSTALL_HOST.md)

> **柴嗅 / ChaiSniffer** 分两部分：**浏览器扩展**（嗅探）+ **辅助应用**（下载、合并、打开播放器）。  
> 从 Edge 商店安装扩展后，仍需单独安装辅助应用。

---

## 下载

| 内容 | 链接 |
|------|------|
| **Windows 安装包** | [Releases · 最新版](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) |
| 测试环境 | [TEST_ENV.md](./TEST_ENV.md) |

安装包通常包含：`native-host/` 文件夹、`setup-bridge.cmd`、内置 `bin/ffmpeg.exe`。

---

## 安装步骤（Windows）

1. 从 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) 下载 zip。
2. **解压到任意文件夹**（如「下载」、`D:\Apps\ChaiSniffer` 等），位置不限。
3. 打开柴嗅 **设置**，复制 **扩展 ID**。
4. 进入解压后的 `native-host` 文件夹，双击 `setup-bridge.cmd`，粘贴扩展 ID。
5. 回到设置页，点 **检查是否安装成功**，各项为 ✓ 即可使用。

> **商店版扩展 ID 与测试版 / 侧载版不同**，安装时必须使用**当前正在用的那份**设置页里的 ID。  
> 扩展 **0.9.17** 请搭配 Host **host-v0.9.17**。在设置中可配置 **下载目录**（成片由辅助应用写入，不依赖浏览器另存为）。

---

## 播放器

在扩展 **播放器设置** 中填写 **[mpv](https://mpv.io/)**（**当前推荐**）、VLC、PotPlayer 等路径。  
**NeoPlayer**（作者自用）仍在开发中，之后会发布 Release；现阶段请优先使用 mpv。

**浮动图标：** 设置 → 嗅探 → **显示视频浮动图标**（v0.9.16+，默认开启，可关闭）。

---

## macOS

扩展嗅探可能可用；辅助应用（下载/播放）**暂未完整支持**，请使用 Windows。

---

## 常见问题

**Q：辅助应用可以装在任何盘吗？**  
A：可以。解压到任意文件夹后，在该文件夹内运行 `setup-bridge.cmd` 即可；脚本会登记实际路径。

**Q：为什么商店扩展还要再装辅助应用？**  
A：商店只能装浏览器部分；下载、写文件、调用播放器需要本机程序。Release 中的辅助应用为 `host.exe`（不含 Python 源码）。

**Q：连接失败 / 下载异常？**  
A：确认扩展 ID 一致、已运行安装脚本、Host 与扩展版本匹配（0.9.17 ↔ host-v0.9.17），并在设置页重新检查。

**Q：等 Edge 商店审核时如何自用新版？**  
A：从 Releases 侧载扩展 zip + 安装同版本 Host；侧载 ID ≠ 商店 ID，需单独登记。
