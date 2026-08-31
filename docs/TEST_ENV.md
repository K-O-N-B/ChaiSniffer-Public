# 测试环境说明

> 供用户预期管理、商店审核备注与问题反馈时对照。  
> 产品：**柴嗅 / ChaiSniffer**

---

## 当前验证环境（主要）

| 项 | 版本 / 说明 |
|----|-------------|
| **操作系统** | Windows 10 / 11（64 位）— **完整功能在此环境验证** |
| **浏览器** | Microsoft Edge（Chromium，Stable 通道） |
| **扩展版本** | 0.9.14+（Manifest V3） |
| **本机 Host** | Release 包 + `setup-bridge.cmd` 登记 |
| **ffmpeg** | Release 内置 `native-host\bin\ffmpeg.exe` |
| **播放器** | mpv（主测）；PotPlayer / VLC 部分路径验证 |
| **下载目录默认** | `%USERPROFILE%\Downloads\mpv-bridge` |

### 已测主流程（Windows）

- [x] 扩展加载、Popup 资源列表、嗅探 HLS / 直链
- [x] B 站分轨嗅探、音画配对、本机混流下载
- [x] HLS AES-128 本机下载（有 ffmpeg）
- [x] Native Host 自检（扩展 / Host / ffmpeg / 播放器）
- [x] 下载临时目录清理
- [x] 浮动图标、多 video 鼠标命中

### 未在 Windows 外完整验收

- [ ] macOS 本机 Host
- [ ] Linux 本机 Host

---

## macOS 支持程度

| 模块 | 状态 |
|------|------|
| Edge / Chrome **扩展**（嗅探、列表） | 理论上可用，**未作为发布目标做系统测试** |
| **本机 Host**（下载、ffmpeg、播放器桥接） | ⏸ **推迟**；**不保证可用** |

Mac 用户请预期：**仅扩展层功能可能可用，本机下载/播放请勿依赖。**

---

## Edge 商店 / 审核测试指引

审核员或新用户可按以下顺序验证（需 Windows）：

1. 安装扩展（商店包或开发者加载）。
2. 从 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) 下载并解压 **Windows 本机组件**。
3. 运行 `native-host\setup-bridge.cmd`，粘贴设置页中的 **扩展 ID**。
4. 扩展 **设置 → 运行完整自检**，应显示 Host / ffmpeg / 播放器 就绪。
5. 打开含 **公开 HLS 测试流** 的页面（或用户自有授权内容），确认 Popup 出现资源并可发起本机下载。

**说明：** 完整下载/播放依赖本机 Host，非扩展单独即可完成。详见 [INSTALL_HOST.md](./INSTALL_HOST.md)。

---

## 反馈问题时请提供

- Windows / macOS 版本
- Edge 版本（`edge://version`）
- 扩展版本（设置页或 `edge://extensions`）
- 是否已安装 Host、自检截图
- 站点类型（如 B 站分轨 / 普通 HLS）
