# Edge Partner Center — 字段复制区

> 打开 [Partner Center → 你的扩展 → Store listing](https://partner.microsoft.com/dashboard/microsoftedge/overview) 后，按字段粘贴。  
> **版本：** 0.9.16

---

## Extension name（扩展名称）

```
柴嗅
```

备用英文名（若表单允许副标题或英文别名）：

```
ChaiSniffer
```

---

## Short description（简短描述，≤ 132 字符）

**中文：**

```
嗅探网页媒体地址，本机下载非 DRM 的 HLS，或交给 mpv 等播放器。需单独安装 Windows 辅助应用。可在设置中关闭视频浮动图标。
```

**English（若需英文短描述）：**

```
Discover media URLs, download non-DRM HLS locally, or open in mpv. Requires separate Windows helper app. Optional video float icon.
```

---

## Description（详细描述）

**中文 — 完整粘贴：**

```
柴嗅（ChaiSniffer）帮助您在浏览网页时发现页面中的流媒体地址（HLS m3u8、DASH mpd、直链等），并在本机完成下载或交给外部播放器播放。

【主要功能】
• 自动识别当前标签页中的媒体资源，在弹出面板中列出
• 视频上可选浮动图标：悬停显示，一键用播放器打开（可在设置中关闭）
• 将地址、Cookie、Referer 传递给本机 mpv、VLC、PotPlayer 等播放器（推荐 mpv）
• 配合 Windows 辅助应用（需从 GitHub 单独下载）可下载非 DRM 的 HLS（含 AES-128）及常见分轨内容
• 内置 m3u8 解析工具、下载任务管理、环境自检
• 明确拒绝 Widevine 等商业 DRM 内容

【重要说明】
1. 本扩展不包含下载合并程序。完整下载/播放能力需安装 Windows 辅助应用（见 GitHub ChaiSniffer-Public Releases）。
2. 从商店安装后，请在扩展「设置」页复制「扩展 ID」，运行辅助应用包中的 setup-bridge.cmd 完成桥接。
3. macOS 上辅助应用暂未完整支持，Mac 用户请勿依赖本机下载功能。
4. 请遵守版权与当地法律，仅处理您有权保存或离线观看的内容。

【隐私】
所有嗅探与下载处理均在您的本机完成；扩展不向开发者服务器上传浏览或媒体数据。详见 GitHub 隐私政策。

测试环境：Windows 10/11 + Microsoft Edge + 辅助应用 + ffmpeg + mpv。
```

**English — full paste:**

```
ChaiSniffer discovers streaming media URLs (HLS, DASH, direct links) on web pages and lets you download or open them with local players on your PC.

Features:
• Lists sniffed media for the active tab
• Optional floating icon on videos (toggle in Settings)
• Passes URL, cookies, and referer to mpv, VLC, PotPlayer, etc. (mpv recommended)
• With the separate Windows helper app (GitHub Releases), downloads non-DRM HLS including AES-128
• Built-in m3u8 tools, download tasks, and setup self-check
• Refuses commercial DRM (Widevine, etc.)

Important:
1. The extension alone does not include ffmpeg or download workers. Install the Windows helper app from GitHub ChaiSniffer-Public Releases.
2. After installing from the store, copy your extension ID from Settings and run setup-bridge.cmd from the helper package.
3. macOS helper app is not fully supported yet.
4. Use only on content you are authorized to access.

Privacy: All sniffing and downloads run locally on your device. No browsing or media data is sent to the developer. See the privacy policy on GitHub.

Tested on Windows 10/11 with Microsoft Edge Stable.
```

---

## Privacy policy URL（隐私政策）

```
https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md
```

简体用户也可链：

```
https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md
```

---

## Support / Contact URL（支持链接）

```
https://github.com/K-O-N-B/ChaiSniffer-Public/issues
```

项目主页（可选）：

```
https://github.com/K-O-N-B/ChaiSniffer-Public
```

---

## Category（分类）

- **Primary / 主要：** Productivity（生产力）或 Developer tools（开发人员工具）
- **Secondary / 次要：** Utilities（实用程序）

---

## Age rating（年龄分级）

建议：**Teen / 13+** 或平台默认「通用」— 扩展不托管第三方内容，用户自行访问网页。

---

## Notes for certification（认证说明）

复制 [EDGE_REVIEW_NOTES.md](./EDGE_REVIEW_NOTES.md) 全文到 Partner Center 的 **Notes for certification** 字段。

---

## Package（上传包）

上传文件：`ChaiSniffer-Extension-v0.9.16.zip`  
（维护者仓库 `dist-release/`，根目录含 `manifest.json`，version `0.9.16`）
