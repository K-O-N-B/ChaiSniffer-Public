# Chrome Web Store — Store listing fields (v0.9.16)

Dashboard: https://chrome.google.com/webstore/devconsole → your item → **Store listing**

---

## Product name

**Primary (English listing — required):**
```
ChaiSniffer
```

If you add a Chinese locale later, use:
```
柴嗅
```

---

## Summary (short description, ≤132 characters)

**English:**
```
Discover media URLs, download non-DRM HLS locally, or open in mpv. Requires separate Windows helper app. Optional video float icon.
```

**Chinese (if locale added):**
```
嗅探网页媒体地址，可本机下载视频，也可以通过本地播放器来播放网络视频，搭配AI、补帧、4K功能，可以使网络视频质量提升。需单独安装 Windows 辅助应用。
```

---

## Description (detailed, English — paste this)

```
ChaiSniffer discovers streaming media addresses on web pages (HLS m3u8, DASH mpd, direct links, etc.) while browsing, and lets you download them locally or hand them off to an external player.

Key features:
• Automatically detects media resources on the active tab and lists them in the popup panel
• Optional floating icon on videos: shown on hover, one click to open in your player (can be turned off in Settings)
• Passes URL, Cookie, and Referer to local players such as mpv, VLC, and PotPlayer (mpv recommended)
• With the Windows helper app (downloaded separately from GitHub), download non-DRM HLS (including AES-128) and common split-track content
• Built-in m3u8 parser, download task manager, and environment self-check
• Explicitly refuses commercial DRM such as Widevine

Important notes:
1. This extension does not include download/mux tools; full capability requires the Windows helper app (GitHub ChaiSniffer-Public Releases).
2. After installing from the store, copy your extension ID on the Settings page and run setup-bridge.cmd to complete the bridge.
3. Picture quality, AI translation, frame interpolation, 4K, and similar features are provided by the player you install, not inside this extension.
4. Please comply with copyright and local laws; only handle content you are authorized to save or watch offline.

All sniffing and downloading is done on your device; browsing and media data are not uploaded to the developer.

Helper app: https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest
Privacy: https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md
```

**Chinese description (optional locale):**
```
柴嗅（ChaiSniffer）帮助您在浏览网页时发现页面中的流媒体地址（HLS m3u8、DASH mpd、直链等），并在本机完成下载或交给外部播放器播放。

主要功能：
• 自动识别当前标签页中的媒体资源，在弹出面板中列出
• 视频上可选浮动图标：悬停显示，一键用播放器打开（可在设置中关闭）
• 将地址、Cookie、Referer 传递给本机 mpv、VLC、PotPlayer 等播放器（推荐 mpv）
• 配合 Windows 辅助应用（需从 GitHub 单独下载）可下载非 DRM 的 HLS（含 AES-128）及常见分轨内容
• 内置 m3u8 解析工具、下载任务管理、环境自检
• 明确拒绝 Widevine 等商业 DRM 内容

重要说明：
1. 本扩展不包含下载合并程序；完整能力需安装 Windows 辅助应用（GitHub ChaiSniffer-Public Releases）。
2. 从商店安装后，请在设置页复制扩展 ID，运行 setup-bridge.cmd 完成桥接。
3. 画质、AI 翻译、补帧、4K 等由您安装的播放器提供，不在本扩展内实现。
4. 请遵守版权与当地法律，仅处理您有权保存或离线观看的内容。

所有嗅探与下载均在您的本机完成，不向开发者上传浏览或媒体数据。
```

---

## Category

```
Productivity
```

(If forced to pick from Chrome’s list, **Tools** or **Productivity** — prefer Productivity.)

---

## Language

Primary: **English**  
Optional additional locales: Chinese (Simplified), Chinese (Traditional)

---

## Official URL / Support URL / Privacy

| Field | Value |
|-------|-------|
| Official URL | `https://github.com/K-O-N-B/ChaiSniffer-Public` |
| Support URL | `https://github.com/K-O-N-B/ChaiSniffer-Public/issues` |
| Privacy policy | `https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md` |

---

## Graphics

| Asset | File |
|-------|------|
| Icon 128×128 | `store-assets\v0.9.16-edge\store-icon-128.png` |
| Screenshots (5) | `01` … `05` in same folder (1280×800) |

---

## Mature content

**No** — do not mark as mature.
